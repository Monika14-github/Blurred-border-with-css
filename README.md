# Blurred-border-with-css
.....html.....
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <div>Thanks for CSS which gave me blurred border.</div>
</html>
.....css.......
@charset "UTF-8";
body {
  display: grid;
  place-content: center;
  margin: 0;
  min-height: 100vh;
}

div {
  display: grid;
  place-content: center;
  position: relative;
  border: solid 0.55em rgba(22, 5, 5, 0.03);
  padding: 0 1em;
  height: 500vmin;
  max-width: 13em;
  max-height: 7em;
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2), 2px 2px 17px rgba(0, 0, 0, 0.35), 2px 2px 25px rgba(0, 0, 0, 0.5);
  background: url(https://wallpapercave.com/wp/xAmWboz.jpg) 50%/cover border-box padding-box;
  color: #000000;
  font: 300 3em/0.75 italic small-caps bold 12px/30px Georgia,serif;
  text-decoration: line-through;
  text-align: center;
  text-shadow: 2px 2px red;
  font-style: italic;
}
div:before {
  position: absolute;
  z-index: -1;
  /* put it *behind* parent */
  /* go outside padding-box by 
   * a border-width ($b) in every direction */
  top: -1.5em;
  right: -1.5em;
  bottom: -1.5em;
  left: -1.5em;
  border: inherit;
  border-color: transparent;
  background: inherit;
  background-clip: border-box;

  -webkit-filter: blur(9px);
  filter: blur(9px);
 
  -webkit-clip-path: inset(0);
  clip-path: inset(0);
  content: "";
}
