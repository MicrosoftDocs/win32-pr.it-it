---
title: Uso di HTML con Windows Media Player
description: Uso di HTML con Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Windows Media Player a oggetti, HTML
- modello a oggetti, HTML
- Windows Media Player ActiveX, HTML per il modello a oggetti
- ActiveX, HTML per il modello a oggetti
- Windows Media Player Controllo mobile ActiveX,HTML per il modello a oggetti
- Windows Media Player Mobile, HTML per il modello a oggetti
- HTML con Windows Media Player
- incorporamento di pagine Web, HTML
- incorporamento, pagine Web
- comandi script
- CAPOVOLGIMENTO DELL'URL
- rich media streaming
- supporto browser
- visualizzazione di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72185dec8ae9a2119d8c3218478e7ebb5a2df4d7740b25c9f4ecc016aa392e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465921"
---
# <a name="using-html-with-windows-media-player"></a>Uso di HTML con Windows Media Player

## <a name="overview"></a>Panoramica

L'uso di HTML Windows Media Player è un ottimo modo per combinare audio e video con testo e grafica. È possibile incorporare il Windows Media Player in una pagina Web quando si vuole integrare il contenuto statico o creare applicazioni Web con supporti digitali. Quando invece si vuole integrare i file multimediali digitali con HTML, è possibile visualizzare le pagine Web in modalità completa del lettore facendovi riferimento in playlist di metafile Windows Media.

Se si scrivono programmi personalizzati che incorporano il controllo Windows Media Player in modalità remota, è anche possibile controllare le pagine Web visualizzate nei vari riquadri della modalità completa del lettore quando gli utenti disancano il controllo. In questo modo è possibile mantenere la continuità tra gli stati ancorati e non ancorati.

## <a name="web-embedding"></a>Incorporamento Web

È possibile usare il controllo Windows Media Player come parte di una pagina Web creata. Vedere [Incorporamento del controllo Windows Media Player in una pagina Web.](embedding-the-windows-media-player-control-in-a-web-page.md)

## <a name="script-commands-and-url-flipping"></a>Comandi script e capovolgimento url

I comandi script sono coppie testo/valore che è possibile incorporare nei file multimediali digitali o nei flussi. È possibile usare i comandi script personalizzati esclusivamente per attivare il codice di script, consentendo Windows Media Player gestire automaticamente altri comandi script.

Quando sono presenti diverse pagine Web che accompagnano una presentazione multimediale digitale, i comandi di script URL possono modificare automaticamente la pagina in un frame mentre il controllo Windows Media Player continua la riproduzione di file multimediali digitali in un altro frame. Questa operazione è detta capovolgimento dell'URL ed è un ottimo modo per creare una presentazione multimediale. Altri comandi script gestiti automaticamente consentono di passare alla riproduzione in un file multimediale o un flusso diverso, visualizzare il testo dei sottotitoli in lingua originale o attivare eventi come gli inserimenti di annunci definiti in una playlist di metafile di Windows Media.

Per altre informazioni sul capovolgimento dell'URL, vedere [Creazione di Web-Based presentazioni.](creating-web-based-presentations.md)

## <a name="rich-media-streaming"></a>Rich Media Streaming

Il capovolgimento dell'URL funziona meglio con pagine semplici che vengono caricate rapidamente. Con le pagine più complesse, più componenti vengono trasferiti singolarmente, rendendo difficile sincronizzare la visualizzazione della pagina con i supporti digitali. Per consentire presentazioni multimediali complesse, le pagine Web possono essere aggiunte a un flusso multimediale e recapitate al lettore allo stesso modo di audio e video. In questo modo è possibile sincronizzare molto più facilmente i componenti della presentazione, soprattutto tramite connessioni a bassa velocità.

Per altre informazioni sul flusso multimediale, vedere [Creating Web-Based Presentations](creating-web-based-presentations.md).

## <a name="browser-support"></a>Supporto browser

È possibile incorporare il Windows Media Player in Microsoft Internet Explorer, Firefox e Netscape Navigator, anche se il processo è leggermente diverso per ognuno. È anche possibile creare pagine Web progettate per funzionare con tutti e tre i browser.

Con Internet Explorer e Firefox, si incorpora il controllo usando l'elemento OBJECT HTML. Lo strumento di navigazione richiede tuttavia un approccio diverso, perché non supporta direttamente i ActiveX personalizzati. Con Lo strumento di navigazione si usa l'elemento APPLET per incorporare una speciale applet Java nella pagina. Questa applet gestisce la comunicazione con il ActiveX lettore.

Per altre informazioni sul supporto di Firefox, vedere [Uso del controllo Windows Media Player con Firefox.](using-the-windows-media-player-control-with-firefox.md)

Per altre informazioni sul Netscape Navigator, vedere [Using Windows Media Player with Netscape 7.1 (Uso di Windows Media Player con Netscape 7.1).](using-windows-media-player-with-netscape-7-1.md)

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Visualizzazione di pagine Web in modalità completa del lettore

È possibile estendere la funzionalità di Windows Media Player o fornire una visualizzazione personalizzata delle informazioni che accompagnano i file multimediali digitali visualizzando le pagine Web in modalità completa del lettore. Questa è la funzionalità HTMLView dei Windows multimediali. I metafile offrono un ottimo controllo sul contenuto della playlist, consentendo di eseguire facilmente la transizione tra clip, inserire annunci e visualizzare immagini fisse in Windows Media Player. Per visualizzare le pagine Web in modalità completa del lettore, usare l'elemento PARAM per aggiungere riferimenti URL alle voci della playlist o a intere playlist.

Per altre informazioni sull'uso delle pagine Web nei metafile, vedere [Visualizzazione di pagine Web in Windows Media Player](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




