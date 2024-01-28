body {
    margin: 0;    
}
#general {
    overflow-y: hidden;
    overflow-x: hidden;
    position: absolute;
    width: 100%;
    height: 100%;    
}
#display{
    text-align: center;
    width: 100%;
    height: 100%;    
    color: white;
}
#visible {
    padding-left: 2%;
    padding-right: 2%;
    font-family: "Arial";
}
#invisible {
    visibility: hidden;
    width: 96%;
    font-family: "Arial";
}
#alert {
    position: absolute;
    text-align: center;
    top: 100%;
    width: 100%;
    height: 15%;
    font-size: 64px;
}
#alert-invisible {
    display: none;
    visibility: hidden;
}
#img64 {
    width: auto;
    height: 100%;
    max-width: 100%;
    position: inherit;
}
span.header {
    display: block;
    margin-bottom: 3vh; /*2.5%*/
    white-space: nowrap;
}

span.page-count {
    font-size: 70%;
    display: block;
    white-space: nowrap;
    text-align: right;
}

.marquee {
    margin: 0 auto;
    white-space: nowrap;
    overflow: hidden;
    box-sizing: border-box;
    border-top: 0px black solid;
}

.marquee span {
    display: inline-block;
    padding-left: 100%;
    text-indent: 0;
    animation: marquee 5s linear infinite;
    -webkit-animation: marquee 5s linear infinite;
}
@keyframes marquee {
    0%   { transform: translate(0, 0); }
    100% { transform: translate(-100%, 0); }
}

.slide_info {
    display: none;
}
