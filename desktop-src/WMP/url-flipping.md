---
title: Capovolgimento URL
description: Capovolgimento URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player, presentazioni basate sul Web
- Modello a oggetti di Windows Media Player, presentazioni basate sul Web
- modello a oggetti, presentazioni basate sul Web
- Presentazioni Windows Media Player per dispositivi mobili, basate sul Web
- Windows Media Player ActiveX Control, presentazioni basate sul Web
- Controllo ActiveX Windows Media Player Mobile, presentazioni basate sul Web
- Controllo ActiveX, presentazioni basate sul Web
- Windows Media Player, capovolgimento URL
- Modello a oggetti di Windows Media Player, capovolgimento degli URL
- modello a oggetti, capovolgimento URL
- Windows Media Player Mobile, capovolgimento URL
- Controllo ActiveX Windows Media Player, capovolgimento URL
- Controllo ActiveX Windows Media Player Mobile, capovolgimento URL
- Controllo ActiveX, capovolgimento URL
- Presentazioni basate sul Web, capovolgimento degli URL
- creazione di presentazioni basate sul Web, capovolgimento degli URL
- Capovolgimento URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "103714722"
---
# <a name="url-flipping"></a>Capovolgimento URL

L'uso di pagine Web per le presentazioni è denominato capovolgimento dell'URL e viene gestito automaticamente da Windows Media Player quando rileva i comandi di script URL incorporati nel flusso multimediale digitale che sta riproducendo. È possibile specificare un frame di destinazione per le pagine in ogni comando di script oppure è possibile specificarlo impostando la proprietà **Settings. defaultFrame** . È possibile impostare questa proprietà nel codice script o usando un elemento PARAM all'interno dell'elemento OBJECT che incorpora il controllo Media Player di Windows.

È possibile gestire i comandi script URL nel codice JScript esattamente come si gestiscono i comandi di script personalizzati. Se si desidera che il controllo Windows Media Player ignori i comandi di script URL, in modo che sia possibile gestirli interamente autonomamente, impostare le *Impostazioni*. proprietà **invokeURLs** su false nel codice script o utilizzando un elemento param come descritto in precedenza.

Nell'esempio seguente viene illustrato un frame tipico per l'capovolgimento degli URL. Per prima cosa, creare una pagina che descrive il frame:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Successivamente, creare il file player.html a cui viene fatto riferimento nel frame con frame usando il codice seguente (si presuppone che il file video. wmv esista nella stessa directory dei file HTML):


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



Se le pagine Web sono sufficientemente piccole da caricare rapidamente, questa configurazione può essere sufficiente per le proprie esigenze. Se, d'altra parte, le pagine Web sono complesse, i flussi multimediali avanzati possono risultare più efficaci a seconda della velocità di connessione dei destinatari.

> [!Note]  
> Il capovolgimento degli URL non funziona correttamente con le pagine visualizzate in Netscape Navigator. Anziché apparire nel frame specificato da **DefaultFrame**, ogni comando script URL ricevuto in Navigator Visualizza l'URL in una nuova finestra del browser.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di presentazioni Web-Based**](creating-web-based-presentations.md)
</dt> <dt>

[**Uso dello script per controllare il capovolgimento degli URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




