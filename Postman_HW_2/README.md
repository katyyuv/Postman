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
OR 
```
pm.test("Body is correct", function () {
    pm.response.to.have.body("This is the first responce from server!ss");
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
5. Check that the age in the response is equal to the age s request (enter the age manually)
```
pm.test("Check age", function () {
    pm.expect(respBody.age).to.eql("21");
});
```
6. Check that the salary in the response is equal to the salary s request (enter the salary manually)
```
pm.test("Check salary", function () {
    pm.expect(respBody.salary).to.eql(400);
});
```
7. Sparse request

`var reqBody = request.data`

8. Check that the name in the response is equal to the name s request (name from the request)
```
var req_Name = reqBody.name
pm.test("Check name is " + req_Name, function () {
    pm.expect(respBody.name).to.eql(req_Name);
});
```
9. Check that the age in the response is equal to the age s request (age from the request)
```
var req_Age = reqBody.age
pm.test("Check age is " + req_Age, function () {
    pm.expect(respBody.age).to.eql(req_Age);
});
```
10. Check that the salary in the response is equal to the salary s request (salary from the request)
```
var req_Salary = reqBody.salary
pm.test("Check salary is " + req_Salary, function () {
    pm.expect(respBody.salary).to.eql(+req_Salary);
});
```
11. Console the family parameter from response.

`console.log(respBody.family)`
12. Check that u_salary_1_5_year in the response is equal to the salary*4 s request (salary from the request)
```
pm.test("Check salary is " + (+req_Salary * 4), function () {
    pm.expect(respBody.family.u_salary_1_5_year).to.eql(+req_Salary * 4);
});
```
