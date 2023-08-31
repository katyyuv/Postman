> http://162.55.220.72:5005/first
1. Send response

`GET http://162.55.220.72:5007/first`

2. Status code 200
```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

3. Check that the correct string comes in the body

```
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server!ss");
});
```

> http://162.55.220.72:5007/user_info_3
1. Send repsonse

`POST http://162.55.220.72:5007/user_info_3`

2. Status code 200
```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```
3. Sparse response body to json

`var respBody = pm.response.json();`

4. Check that the name in the response is equal to the name s request (enter the name manually)
```
pm.test("Check Name", function () {
    pm.expect(respBody.name).to.eql("Kate");
});
```
