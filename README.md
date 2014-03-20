Check out a demo [here](http://stolksdorf.github.io/Domjs).

# What is it
Dom.js is a light-weight DOM node creation library inspired by [Facebook's React](http://facebook.github.io/react/). It has no dependacies and is about 20 lines.

# How to use
Just include the lib and anywhere you need to create DOM elements in just Javascript, use Dom.js. the `DOM()` takes `1 + n` arguements. First beigns an attributes object and then as many child elements you want, that could be other calls to `DOM()` or just text nodes.

	DOM.div({class:'cool_cssClass'}, "Hello ", DOM.span({}, 'World'));

You can use React's live [JSX Compiler](http://facebook.github.io/react/jsx-compiler.html) to help you convert your exsisting HTML into a javascript format.

# Examples
Kitten Linker

	var kittens = DOM.a({href:'http://placekitten.com', target:'_blank'},
		DOM.img({src:'http://placekitten.com/200/300'})
	);
	$(example).append(kittens);

Simple Form

	DOM.form({action:"demo_form.asp"},
		"First name: ", DOM.input({type:"text", name:"first_name"}), DOM.br(),
		"Last name: ", DOM.input({type:"text", name:"last_name"}), DOM.br(),
		DOM.input({ type:"submit", value:"Submit"})
	)


# Supported Node Types
I included nearly every type I could find, but if I missed one feel free to add it in. They're simply stored as an array in the source code.

	a,abbr,acronym,address,applet,area,article,aside,audio,b,base,basefont,bdi,bdo,bgsound,big,blink,blockquote,body,br,button,canvas,caption,center,cite,code,col,colgroup,content,data,datalist,dd,decorator,del,details,dfn,dir,div,dl,dt,element,em,embed,fieldset,figcaption,figure,font,footer,form,frame,frameset,h1,h2,h3,h4,h5,h6,head,header,hgroup,hr,html,i,iframe,img,input,ins,isindex,kbd,keygen,label,legend,li,link,listing,main,map,mark,marquee,menu,menuitem,meta,meter,nav,nobr,noframes,noscript,object,ol,optgroup,option,output,p,param,plaintext,pre,progress,q,rp,rt,ruby,s,samp,script,section,select,shadow,small,source,spacer,span,strike,strong,style,sub,summary,sup,table,tbody,td,template,textarea,tfoot,th,thead,time,title,tr,track,tt,u,ul,var,video,wbr,xmp

