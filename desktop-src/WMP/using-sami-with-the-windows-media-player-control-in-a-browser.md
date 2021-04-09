---
title: Uso di SAMI con il controllo Media Player Windows in un browser
description: Uso di SAMI con il controllo Media Player Windows in un browser
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- SAMI (Synchronized Accessible Media Interchange), file
- SAMI (interscambio multimediale accessibile sincronizzato), file
- SAMI (Synchronized Accessible Media Interchange), codice di esempio
- SAMI (interscambio multimediale accessibile sincronizzato), codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955807"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="1b369-114">Uso di SAMI con il controllo Media Player Windows in un browser</span><span class="sxs-lookup"><span data-stu-id="1b369-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="1b369-115">Anziché creare un file SAMI per ogni lingua o stile del tipo di carattere, è possibile dichiarare classi di stile diverse in un file usando gli script di base e il modello a oggetti del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="1b369-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="1b369-116">È possibile creare controlli personalizzati che consentono all'utente di scegliere tra le diverse opzioni relative allo stile e alla lingua.</span><span class="sxs-lookup"><span data-stu-id="1b369-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="1b369-117">Inoltre, si ha il controllo completo sulla progettazione dell'interfaccia del lettore e sulla personalizzazione di ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="1b369-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="1b369-118">Per informazioni dettagliate sull'incorporamento del controllo Windows Media Player in una pagina Web, vedere [semplice esempio di scripting in una pagina Web](simple-example-of-scripting-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="1b369-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="1b369-119">Nell'esempio di codice seguente viene illustrato come utilizzare sottotitoli con il controllo Media Player Windows incorporato in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="1b369-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="1b369-120">Include i controlli che consentono all'utente di selezionare lo stile e la lingua del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="1b369-120">It includes controls to allow the user to select font style and language.</span></span>


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="1b369-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b369-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b369-122">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="1b369-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




