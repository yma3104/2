var chime;

var sounds = [];

function preload() {
  soundFormats('m4a');
  for (var i = 0; i < 15; i++) {
    let sound = loadSound('glockenspiel.m4a');
    sound.rate(0.5 * pow(2, i / 12)); // 12-semitone exponential scale

    sounds.push(sound);
  }
}

function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
}

function draw() {
  background(400);
  noFill();

  for (var i = 0; i < sounds.length; i++) {
    let sound = sounds[i];
    if (sound.isPlaying()) {
      map(sound.currentTime(), 0, sound.duration(), 255, 220);
      for (var x = 10; x < 390; x = x + 40) {
      ellipse(width / sounds. length * (i + 1), 200, x + 20);
      }
    }
  }
}

function mouseMoved() {
  if (mouseY < 40, mouseY > 0) {
    sounds[0].play();
  }
  if (mouseY < 80, mouseY > 40) {
    sounds[1].play();
  }
  if (mouseY < 120, mouseY > 80) {
    sounds[2].play();
  }
  if (mouseY < 160, mouseY > 120) {
    sounds[3].play();
  }
  if (mouseY < 200, mouseY > 160) {
    sounds[4].play();
  }
  if (mouseY < 240, mouseY > 200) {
    sounds[5].play();
  }
  if (mouseY < 280, mouseY > 200) {
    sounds[6].play();
  }
  if (mouseY < 320,mouseY > 280) {
    sounds[7].play();
  }
  if (mouseY < 360, mouseY > 320) {
    sounds[8].play();
  }
  if (mouseY < 400, mouseY > 360) {
    sounds[8].play();
  }
}
