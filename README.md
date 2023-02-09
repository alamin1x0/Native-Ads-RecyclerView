# native_template_recyclerview

## Extrace the file

1. Add as a new modoule.
2. Implement in build.gradle(app)

```
    implementation project(':nativetemplates')
```

<br/>
3. Use in your recyclerview
<br/>
<br/>
Java

```

private List<UserModel> list;
private UserAdapter adapter;
list = dbDao.getAllUser();
adapter = new UserAdapter(getApplicationContext(), list);

       admobNativeAdAdapter = AdmobNativeAdAdapter.Builder.with(
                getApplicationContext().getString(R.string.admob_native_id),
                adapter,
                "small"   // "medium" it can also used
        ).adItemInterval(1).build();

        binding.recylcerView.setAdapter(admobNativeAdAdapter);

kotlin

```
      val adapter = CustomeAdapter(context, list)
      val admobNativeAdAdapter = AdmobNativeAdAdapter.Builder.with(
            requireContext().resources.getString(R.string.native_id),
            adapter,
            "small"   // "medium" it can also used
        ).adItemInterval(4).build()
      binding.recyclerview.adapter = admobNativeAdAdapter
```

