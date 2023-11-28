// make sure you have selected a environment variable in postman
function isValid() {
    return [200, 201, 202].includes(pm.response.code);
}

function handleResponse(json) {
    for (let property in json) {
        pm.environment.set(property, json[property]);
    }
}

if (!isValid()) {
    console.log("Error in request");
} else {
    let jsonData = pm.response.json();
    //set response in environment variable
    handleResponse(jsonData);


}
