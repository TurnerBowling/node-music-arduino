var restify = require('restify');

var music = require('./music');



var HappyBirthday = [{n: "g", d: 200, r: 10}, {n: "g", d: 200, r: 0}, {n: "a", d: 200, r: 0}, {n: "g", d: 200, r:0}, {n: "c", d: 200, r:0}, {n: "b", d: 400, r:0}, {n: "g", d: 200, r: 10}, {n: "g", d: 200, r: 0}, {n: "a", d: 200, r: 0}];


var server = restify.createServer({
  name: 'myapp',
  version: '1.0.0'
});
server.use(restify.acceptParser(server.acceptable));
server.use(restify.queryParser());
server.use(restify.bodyParser());

server.get('/echo/:name', function (req, res, next) {
if(req.params.name === "turner")
{
	res.send("hi turner");
	console.log("hi turner");

}else if(req.params.name === "birthday_person") {
	res.send("Happy Birthday!");
	console.log("Happy Birthday!\n *plays happy birthday*");
	music.player(HappyBirthday, music.player);

} else if(req.params.name === "bryan") {
	res.send("Hi bryan");
console.log("hi bryan");
} else {
	res.send("Error: Blinking!");	
}

 // res.send(req.params.);
  return next();
});

server.listen(8080, function () {
  console.log('%s listening at %s', server.name, server.url);
});
