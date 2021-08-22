---
title: Capovolgimento url
description: Capovolgimento url
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player, presentazioni basate sul Web
- Windows Media Player modello a oggetti, presentazioni basate sul Web
- modello a oggetti, presentazioni basate sul Web
- Windows Media Player Presentazioni basate sul Web per dispositivi mobili
- Windows Media Player ActiveX, presentazioni basate sul Web
- Windows Media Player Controllo ActiveX per dispositivi mobili, presentazioni basate sul Web
- ActiveX, presentazioni basate sul Web
- Windows Media Player,CAPOVOLGIMENTO URL
- Windows Media Player a oggetti, capovolgimento dell'URL
- modello a oggetti, capovolgimento dell'URL
- Windows Media Player Mobile, capovolgimento url
- Windows Media Player ActiveX, capovolgimento dell'URL
- Windows Media Player Controllo ActiveX mobile, capovolgimento dell'URL
- ActiveX controllo, capovolgimento dell'URL
- Presentazioni basate sul Web, capovolgimento dell'URL
- creazione di presentazioni basate sul Web, capovolgimento dell'URL
- Capovolgimento dell'URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4471045506447b93621578f27e2f156bb214016b3fa8ec114a689b919314d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134524"
---
# <a name="url-flipping"></a>Capovolgimento url

L'uso di pagine Web per le presentazioni è detto capovolgimento dell'URL e viene gestito automaticamente da Windows Media Player quando rileva comandi di script URL incorporati nel flusso multimediale digitale in riproduzione. È possibile specificare un frame di destinazione per le pagine in ogni comando script oppure impostando la **proprietà Impostazioni.defaultFrame.** È possibile impostare questa proprietà nel codice script o usando un elemento PARAM all'interno dell'elemento OBJECT che incorpora il Windows Media Player controllo.

È possibile gestire i comandi di script URL nel codice JScript proprio come si gestirebbero i comandi di script personalizzati. Se si vuole che il Windows Media Player ignori i comandi di script URL in modo che sia possibile gestirli completamente da soli, impostare la proprietà *Impostazioni*. **invokeURLs** su false nel codice di script o usando un elemento PARAM come descritto in precedenza.

L'esempio seguente illustra un set di frame tipico per l'inversione dell'URL. Creare prima di tutto una pagina che descriva il set di frame:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Creare quindi il file player.html a cui si fa riferimento nel set di frame usando il codice seguente (si presuppone che il file video.wmv esista nella stessa directory dei file HTML):


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



Se le pagine Web sono sufficientemente piccole da essere caricate rapidamente, questa configurazione potrebbe essere sufficiente per le proprie esigenze. Se invece le pagine Web sono complesse, lo streaming multimediale può essere più efficace a seconda della velocità di connessione del pubblico.

> [!Note]  
> Il capovolgimento dell'URL non funziona correttamente con le pagine visualizzate Netscape Navigator. Anziché essere visualizzato nel frame specificato da **defaultFrame,** ogni comando di script URL ricevuto in Navigator visualizza l'URL in una nuova finestra del browser.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di Web-Based presentazioni**](creating-web-based-presentations.md)
</dt> <dt>

[**Uso dello script per controllare il capovolgimento dell'URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




