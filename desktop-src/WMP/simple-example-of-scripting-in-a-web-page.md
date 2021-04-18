---
title: Esempio semplice di scripting in una pagina Web
description: Esempio semplice di scripting in una pagina Web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Controllo ActiveX di Windows Media Player, esempio di scripting
- Controllo ActiveX Windows Media Player Mobile, esempio di scripting
- Controllo ActiveX, esempio di scripting
- incorporamento, pagine Web
- Incorporamento di pagine Web, esempio di scripting
- esempio di script per l'incorporamento di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299015"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="a2b56-119">Esempio semplice di scripting in una pagina Web</span><span class="sxs-lookup"><span data-stu-id="a2b56-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="a2b56-120">È possibile incorporare facilmente il controllo Media Player di Windows in un file HTML usando qualsiasi linguaggio di script riconosciuto dal browser.</span><span class="sxs-lookup"><span data-stu-id="a2b56-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="a2b56-121">Nell'esempio seguente viene utilizzato Microsoft JScript per creare una pagina in cui verrà riprodotto un file quando si fa clic su un pulsante e si interrompe la riproduzione del file quando si fa clic su un altro pulsante.</span><span class="sxs-lookup"><span data-stu-id="a2b56-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="a2b56-122">È possibile incorporare il controllo ActiveX di Windows Media Player in una pagina Web usando i quattro passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2b56-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="a2b56-123">Creare la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="a2b56-123">Create the webpage.</span></span>
2.  <span data-ttu-id="a2b56-124">Aggiungere il tag OBJECT.</span><span class="sxs-lookup"><span data-stu-id="a2b56-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="a2b56-125">Aggiungere un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a2b56-125">Add a user interface.</span></span> <span data-ttu-id="a2b56-126">In questo caso, due pulsanti.</span><span class="sxs-lookup"><span data-stu-id="a2b56-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="a2b56-127">Aggiungere alcune righe di codice per rispondere quando l'utente fa clic su uno dei pulsanti creati.</span><span class="sxs-lookup"><span data-stu-id="a2b56-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="a2b56-128">Creazione della pagina Web</span><span class="sxs-lookup"><span data-stu-id="a2b56-128">Creating the Web Page</span></span>

<span data-ttu-id="a2b56-129">Il primo passaggio consiste nel creare una pagina Web HTML valida.</span><span class="sxs-lookup"><span data-stu-id="a2b56-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="a2b56-130">Il codice seguente è il requisito minimo necessario per creare una pagina HTML vuota ma valida:</span><span class="sxs-lookup"><span data-stu-id="a2b56-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="a2b56-131">Aggiunta del tag OBJECT</span><span class="sxs-lookup"><span data-stu-id="a2b56-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="a2b56-132">Dopo aver creato una pagina Web, è necessario aggiungere un tag OBJECT.</span><span class="sxs-lookup"><span data-stu-id="a2b56-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="a2b56-133">Identifica il controllo ActiveX per il browser e configura le definizioni iniziali.</span><span class="sxs-lookup"><span data-stu-id="a2b56-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="a2b56-134">È necessario inserire il tag OBJECT nel corpo del codice.</span><span class="sxs-lookup"><span data-stu-id="a2b56-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="a2b56-135">Se lo si inserisce nel corpo, l'interfaccia utente predefinita di Windows Media Player sarà visibile.</span><span class="sxs-lookup"><span data-stu-id="a2b56-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="a2b56-136">Se si desidera creare un'interfaccia utente personalizzata, impostare gli attributi Height e Width su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a2b56-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="a2b56-137">È anche possibile impostare il *lettore*. proprietà **uiMode** su "invisibile" quando si desidera nascondere il controllo, ma si riserva comunque spazio per l'oggetto nella pagina.</span><span class="sxs-lookup"><span data-stu-id="a2b56-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="a2b56-138">Il codice seguente è consigliato quando si fornisce un'interfaccia utente personalizzata:</span><span class="sxs-lookup"><span data-stu-id="a2b56-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="a2b56-139">Sono necessari gli attributi di tag OBJECT seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2b56-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="a2b56-140">ID</span><span class="sxs-lookup"><span data-stu-id="a2b56-140">ID</span></span>

<span data-ttu-id="a2b56-141">Nome che verrà usato da altre parti del codice per identificare e usare il controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a2b56-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="a2b56-142">È possibile scegliere qualsiasi nome, purché sia un nome che non sia già usato da HTML, da estensioni HTML o dal linguaggio di scripting in uso.</span><span class="sxs-lookup"><span data-stu-id="a2b56-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="a2b56-143">In questo esempio viene usato il nome "Player", ma è anche possibile denominarlo "riproduzione" o un altro elemento.</span><span class="sxs-lookup"><span data-stu-id="a2b56-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="a2b56-144">È sufficiente scegliere un nome univoco per la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="a2b56-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="a2b56-145">CLASSID</span><span class="sxs-lookup"><span data-stu-id="a2b56-145">CLASSID</span></span>

<span data-ttu-id="a2b56-146">Numero esadecimale molto grande univoco per il controllo.</span><span class="sxs-lookup"><span data-stu-id="a2b56-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="a2b56-147">Un solo controllo ha questo numero ed è il controllo ActiveX di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a2b56-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="a2b56-148">Per evitare errori tipografici, è possibile copiare e incollare questo numero dalla documentazione.</span><span class="sxs-lookup"><span data-stu-id="a2b56-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="a2b56-149">Le versioni del controllo Windows Media Player precedenti alla versione 7,0 hanno un CLASSId diverso.</span><span class="sxs-lookup"><span data-stu-id="a2b56-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="a2b56-150">Aggiunta di un'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a2b56-150">Adding a User Interface</span></span>

<span data-ttu-id="a2b56-151">HTML consente un'ampia gamma di elementi dell'interfaccia utente, consentendo all'utente di interagire con la pagina Web facendo clic, premendo i tasti e altre azioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a2b56-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="a2b56-152">L'aggiunta di alcuni pulsanti di INPUT è il modo più semplice per fornire un'interfaccia utente rapida.</span><span class="sxs-lookup"><span data-stu-id="a2b56-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="a2b56-153">Il codice seguente crea due pulsanti che possono rispondere all'utente.</span><span class="sxs-lookup"><span data-stu-id="a2b56-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="a2b56-154">Quando si fa clic su un pulsante, viene avviata la riproduzione del flusso multimediale e l'altro pulsante lo arresta:</span><span class="sxs-lookup"><span data-stu-id="a2b56-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="a2b56-155">Il nome del pulsante viene usato per identificare il pulsante al codice. il valore è l'etichetta che verrà visualizzata sul pulsante e l'attributo OnClick identifica la parte del codice di scripting che verrà chiamata quando si fa clic sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="a2b56-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="a2b56-156">Aggiunta di codice di script</span><span class="sxs-lookup"><span data-stu-id="a2b56-156">Adding Scripting Code</span></span>

<span data-ttu-id="a2b56-157">Il codice di scripting consente di aggiungere interattività alla pagina.</span><span class="sxs-lookup"><span data-stu-id="a2b56-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="a2b56-158">Il codice di scripting può rispondere a eventi, chiamare metodi e modificare le proprietà della fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a2b56-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="a2b56-159">Gli script estesi sono racchiusi in un set di tag di SCRIPT.</span><span class="sxs-lookup"><span data-stu-id="a2b56-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="a2b56-160">Il tag SCRIPT indica al browser dove si trova il codice di script e identifica il linguaggio di scripting.</span><span class="sxs-lookup"><span data-stu-id="a2b56-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="a2b56-161">Se non si identifica una lingua, la lingua predefinita sarà Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="a2b56-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="a2b56-162">È consigliabile racchiudere lo script nei tag di commento HTML, in modo che i browser che non supportano lo script non eseguano il rendering del codice come testo.</span><span class="sxs-lookup"><span data-stu-id="a2b56-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="a2b56-163">Inserire il tag SCRIPT in un punto qualsiasi all'interno del corpo del file HTML e incorporare il codice con commento racchiuso tra i tag di SCRIPT di apertura e chiusura.</span><span class="sxs-lookup"><span data-stu-id="a2b56-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="a2b56-164">Nell'esempio di codice Microsoft JScript seguente viene chiamato il controllo Media Player Windows ed eseguita un'azione appropriata in risposta al clic del pulsante corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a2b56-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="a2b56-165">La funzione di esempio, StartMeUp, viene chiamata quando si fa clic sul pulsante contrassegnato Play e la funzione ShutMeDown viene chiamata quando si fa clic sul pulsante Interrompi.</span><span class="sxs-lookup"><span data-stu-id="a2b56-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="a2b56-166">Il codice all'interno di StartMeUp usa la proprietà URL per definire un percorso al supporto.</span><span class="sxs-lookup"><span data-stu-id="a2b56-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="a2b56-167">Il supporto inizierà immediatamente a riprodursi.</span><span class="sxs-lookup"><span data-stu-id="a2b56-167">The media will start playing immediately.</span></span>

<span data-ttu-id="a2b56-168">Il codice ShutMeDown chiama il metodo **Stop** dell'oggetto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="a2b56-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="a2b56-169">Si noti che l'oggetto **Controls** viene chiamato tramite la proprietà **Controls** dell'oggetto **Player** , che ha il valore ID "Player".</span><span class="sxs-lookup"><span data-stu-id="a2b56-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="a2b56-170">L'esempio seguente illustra un esempio completo.</span><span class="sxs-lookup"><span data-stu-id="a2b56-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="a2b56-171">Si noti che è necessario fornire un URL valido a un nome di file valido nella proprietà URL.</span><span class="sxs-lookup"><span data-stu-id="a2b56-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="a2b56-172">In questo caso il presupposto è che il file Laure. WMA si trovi nella stessa directory del file HTML.</span><span class="sxs-lookup"><span data-stu-id="a2b56-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2b56-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2b56-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2b56-174">**Uso del controllo Media Player di Windows in una pagina Web**</span><span class="sxs-lookup"><span data-stu-id="a2b56-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




