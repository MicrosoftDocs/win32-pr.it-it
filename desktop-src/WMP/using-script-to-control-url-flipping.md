---
title: Uso dello script per controllare il capovolgimento dell'URL
description: Uso dello script per controllare il capovolgimento dell'URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, presentazioni basate sul Web
- Windows Media Player a oggetti, presentazioni basate sul Web
- modello a oggetti, presentazioni basate sul Web
- Windows Media Player Presentazioni per dispositivi mobili basate sul Web
- Windows Media Player ActiveX, presentazioni basate sul Web
- Windows Media Player Controllo ActiveX per dispositivi mobili, presentazioni basate sul Web
- ActiveX controllo, presentazioni basate sul Web
- Windows Media Player,CAPOVOLGIMENTO URL
- Windows Media Player a oggetti, capovolgimento URL
- modello a oggetti, capovolgimento url
- Windows Media Player Mobile, CAPOVOLGIMENTO URL
- Windows Media Player ActiveX controllo, capovolgimento url
- Windows Media Player Mobile ActiveX control,URL fliping
- ActiveX controllo, capovolgimento url
- Presentazioni basate sul Web, capovolgimento url
- creazione di presentazioni basate sul Web, capovolgimento url
- CAPOVOLGIMENTO DELL'URL
- Windows Media Player, rich media streaming
- Windows Media Player a oggetti, rich media streaming
- modello a oggetti, rich media streaming
- Windows Media Player Streaming multimediale per dispositivi mobili
- Windows Media Player ActiveX, flusso multimediale completo
- Windows Media Player Controllo ActiveX per dispositivi mobili, streaming multimediale completo
- ActiveX, flusso multimediale completo
- Presentazioni basate sul Web, rich media streaming
- creazione di presentazioni basate sul Web, rich media streaming
- rich media streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9470bf2b812d36bceb6159ab089e3b08c49bc84515320872b125ed6519568141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507131"
---
# <a name="using-script-to-control-url-flipping"></a>Uso dello script per controllare il capovolgimento dell'URL

Quando un utente si connette a un flusso multimediale completo mentre il flusso è già in corso, è possibile che la pagina Web trasmessa venga visualizzata prima che tutti gli elementi siano arrivati e memorizzati nella cache se Windows Media Player richiama automaticamente l'URL. In questo caso, l'utente visualizza una pagina Web vuota o incompleta fino all'arrivo del set di dati successivo nella cache.

È possibile evitare di visualizzare una pagina Web vuota o incompleta richiamando l'URL usando lo script Windows Media Player di farlo automaticamente. In questo modo, è possibile ignorare il primo capovolgimento dell'URL e quindi richiamare gli URL successivi usando il codice script.

> [!Note]  
> In questa sezione si presuppone che il codice HTML sia in streaming con Windows Media Encoder 9 Series SDK e che il flusso HTML sia stato impostato per la ripetizione.

 

In primo luogo, è necessario creare una pagina Web del set di frame per contenere il frame con il lettore incorporato e il frame che visualizza il codice HTML di streaming. Ognuno di questi due frame inizialmente visualizza una pagina Web separata, quindi si creerà un totale di tre pagine Web. Il codice di esempio seguente illustra la pagina Web del set di frame:


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



L'esempio di pagina Web precedente incorpora due frame. Il primo frame viene visualizzato nella metà sinistra della finestra del browser e visualizza la pagina Web denominata embed \_player.htm. Il codice di esempio seguente crea questa pagina Web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



Il secondo frame nel set di frame viene visualizzato nella metà destra della finestra del browser e visualizza una pagina Web denominata "blank.htm". Il codice di esempio seguente crea questa pagina Web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Quando la pagina del set di frame viene caricata nel browser, il frame sinistro mostra il lettore incorporato e il frame destro mostra il testo "Caricamento in corso..." per informare l'utente che altri dati sono in arrivo. Quando il primo comando di script URL arriva dal flusso HTML, il gestore eventi modifica semplicemente il valore del flag **booleano.** Quando ogni comando di script URL successivo arriva dal flusso HTML, lo script nel gestore eventi carica il nuovo URL nel frame denominato "content" e la pagina Web completa viene visualizzata nel frame situato nella metà destra della finestra del browser.

Per altre informazioni sullo streaming DI HTML Windows Media, vedere l'Windows Media Encoder SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Rich Media Streaming**](rich-media-streaming.md)
</dt> <dt>

[**CAPOVOLGIMENTO URL**](url-flipping.md)
</dt> </dl>

 

 




