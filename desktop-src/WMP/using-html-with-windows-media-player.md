---
title: Uso di HTML con Windows Media Player
description: Uso di HTML con Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Modello a oggetti di Windows Media Player, HTML
- modello a oggetti, HTML
- Controllo ActiveX di Windows Media Player, HTML per il modello a oggetti
- Controllo ActiveX, HTML per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, HTML per il modello a oggetti
- Windows Media Player Mobile, HTML per il modello a oggetti
- HTML con Windows Media Player
- Incorporamento di pagine Web, HTML
- incorporamento, pagine Web
- comandi script
- Capovolgimento URL
- streaming multimediale avanzato
- supporto browser
- visualizzazione di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856262"
---
# <a name="using-html-with-windows-media-player"></a>Uso di HTML con Windows Media Player

## <a name="overview"></a>Panoramica

Usare HTML con Windows Media Player è un ottimo modo per combinare audio e video con testo e grafica. È possibile incorporare il controllo Windows Media Player in una pagina Web quando si desidera integrare il contenuto statico o creare applicazioni Web con supporti digitali. Quando si desidera integrare i supporti digitali con HTML, d'altra parte, è possibile visualizzare le pagine Web nella modalità completa del lettore facendovi riferimento nelle playlist di Windows Media Metafile.

Se si scrivono programmi personalizzati che incorporano il controllo Windows Media Player in modalità remota, è anche possibile controllare le pagine Web visualizzate nei vari riquadri della modalità completa del lettore quando gli utenti disancorano il controllo. Ciò consente di mantenere la continuità tra gli stati ancorati e non ancorati.

## <a name="web-embedding"></a>Incorporamento Web

È possibile utilizzare il controllo Media Player Windows come parte di una pagina Web creata. Vedere [incorporare il controllo Windows Media Player in una pagina Web](embedding-the-windows-media-player-control-in-a-web-page.md).

## <a name="script-commands-and-url-flipping"></a>Comandi script e capovolgimento URL

I comandi script sono coppie di testo/valore che è possibile incorporare nei file multimediali digitali o nei flussi. È possibile utilizzare i comandi di script personalizzati esclusivamente per attivare il codice dello script, consentendo a Windows Media Player di gestire automaticamente altri comandi di script.

Quando sono presenti diverse pagine Web che accompagnano una presentazione multimediale digitale, i comandi script URL possono modificare automaticamente la pagina in un frame mentre il controllo Media Player Windows continua a riprodurre file multimediali digitali in un altro frame. Questa operazione è denominata capovolgimento degli URL ed è un ottimo modo per creare una presentazione multimediale. Altri comandi script gestiti automaticamente consentono di passare dalla riproduzione a un altro file multimediale o flusso, visualizzare il testo della didascalia o generare eventi, ad esempio inserimenti ad, definiti in una playlist Windows Media Metafile.

Per ulteriori informazioni sul capovolgimento degli URL, vedere la pagina relativa alla [creazione di presentazioni Web-Based](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Streaming multimediale avanzato

Il capovolgimento degli URL funziona meglio con pagine semplici che si caricano rapidamente. Con pagine più complesse, più componenti vengono trasferiti singolarmente, rendendo difficile la sincronizzazione della visualizzazione delle pagine con supporti digitali. Per consentire presentazioni multimediali complesse complesse, le pagine Web possono essere aggiunte a un flusso multimediale e distribuite al lettore in modo analogo a audio e video. In questo modo è possibile sincronizzare i componenti della presentazione in modo molto più semplice, soprattutto su connessioni a bassa velocità.

Per ulteriori informazioni sui flussi multimediali avanzati, vedere la pagina relativa alla [creazione di presentazioni Web-Based](creating-web-based-presentations.md).

## <a name="browser-support"></a>Supporto browser

È possibile incorporare il controllo Windows Media Player in Microsoft Internet Explorer, Firefox e Netscape Navigator, sebbene il processo sia leggermente diverso per ognuno di essi. È anche possibile creare pagine Web progettate per funzionare con tutti e tre i browser.

Con Internet Explorer e Firefox, il controllo viene incorporato usando l'elemento oggetto HTML. Il navigatore richiede un approccio diverso, tuttavia, perché non supporta direttamente i controlli ActiveX. Con Navigator si usa l'elemento APPLET per incorporare una speciale applet Java nella pagina. Questa applet gestisce la comunicazione con il controllo ActiveX del lettore.

Per ulteriori informazioni sul supporto di Firefox, vedere [utilizzo del controllo Windows Media Player con Firefox](using-the-windows-media-player-control-with-firefox.md).

Per altre informazioni sul supporto di Netscape Navigator, vedere [uso di Windows Media Player con netscape 7,1](using-windows-media-player-with-netscape-7-1.md).

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Visualizzazione di pagine Web in modalità completa del lettore

È possibile estendere le funzionalità di Windows Media Player o fornire una visualizzazione personalizzata delle informazioni che accompagnano i supporti digitali visualizzando le pagine Web in modalità completa del lettore. Si tratta della funzionalità HTMLView di metafile di Windows Media. I metafile offrono un ottimo controllo sul contenuto della playlist, consentendo di eseguire facilmente la transizione tra clip, inserire annunci e visualizzare immagini ancora in Windows Media Player. Per visualizzare le pagine Web nella modalità completa del lettore, usare l'elemento PARAM per aggiungere riferimenti URL alle voci della playlist o a intere playlist.

Per ulteriori informazioni sull'utilizzo di pagine Web in metafile, vedere [visualizzazione di pagine Web in Windows Media Player](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




