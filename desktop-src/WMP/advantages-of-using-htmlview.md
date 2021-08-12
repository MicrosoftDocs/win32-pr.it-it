---
title: Vantaggi dell'uso di HTMLView
description: Vantaggi dell'uso di HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Windows Playlist di metafile multimediali,vantaggi di HTMLView
- playlist, vantaggi di HTMLView
- playlist di metafile,vantaggi di HTMLView
- Windows Playlist di metafile multimediali,vantaggi di HTMLView
- playlist, vantaggi di HTMLView
- playlist di metafile, vantaggi di HTMLView
- vantaggi di HTMLView
- Windows Media Player,vantaggi di HTMLView
- Windows Media Player,VANTAGGI DI HTMLView
- HTMLView,vantaggi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6019ec83466be9f4eca649d870422dce640fddc3ff011c46c6f918a1a09faa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583268"
---
# <a name="advantages-of-using-htmlview"></a>Vantaggi dell'uso di HTMLView

La funzionalità HTMLView semplifica la creazione di un'esperienza utente integrata basata sul Web che riproduce il contenuto multimediale digitale usando l'aspetto familiare del Web. Quando si combinano contenuto basato sul Web con contenuto multimediale digitale nell'interfaccia utente di Windows Media Player, il risultato può avere un impatto maggiore sull'utente rispetto a quando gli elementi vengono visualizzati separatamente. Il contenuto multimediale digitale è migliorato da informazioni correlate interessanti, mentre la pagina Web può fornire collegamenti a contenuti simili, creando così nuove opportunità di business.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView offre un'esperienza utente migliore

Gli utenti vogliono e apprezzano l'accesso alle informazioni che possono essere offerte con contenuti multimediali digitali, ma non vogliono gestire una serie apparentemente infinita di annunci popup. L'uso di finestre del browser popup per visualizzare annunci pubblicitari sul Web è diventato così comune che è ora disponibile un software che impedisce l'apertura di queste finestre. Questo software può avere l'effetto collaterale indesiderato di impedire la visualizzazione di pagine Web legittime, talvolta sopprimendo un'intera presentazione multimediale digitale.

Quando si usa la funzionalità HTMLView, gli utenti non devono più gestire le finestre popup. Invece di dover aprire una finestra del browser separata per fornire informazioni aggiuntive all'utente, è possibile visualizzare contenuto personalizzato basato sul Web nella funzionalità In riproduzione dell'interfaccia utente di Windows Media Player durante la riproduzione del contenuto audio o video che l'utente desidera.  Gli utenti possono controllare la riproduzione usando i Windows Media Player controllo. Poiché il contenuto viene riprodotto nel lettore in modalità completa, il software progettato per impedire agli annunci popup non impedisce agli utenti di usufruire del contenuto.

## <a name="htmlview-content-is-easy-to-create"></a>Il contenuto di HTMLView è facile da creare

Come suggerisce il nome della funzionalità, si crea contenuto basato sul Web visualizzato usando la funzionalità HTMLView usando Hypertext Markup Language (HTML). Se si crea già contenuto per il Web, non è necessario apprendere un nuovo linguaggio di programmazione per creare facilmente contenuto rtf con la funzionalità HTMLView. Se sono già presenti pagine Web con un controllo Windows Media Player ActiveX incorporato, è possibile fare in modo che queste pagine vengano visualizzate nell'interfaccia utente di Player semplicemente puntando a queste pagine Web da un metafile multimediale Windows Media (file con estensione asx) usando un parametro speciale.

Windows Media Player un'istanza incorporata di Microsoft Internet Explorer per visualizzare il contenuto HTMLView. Ciò significa che non è necessario prendere in considerazione browser Internet diversi, più modelli di scripting o linguaggi di scripting diversi durante la creazione delle pagine Web. Anche se l'utente non usa Internet Explorer browser predefinito, la pagina Web viene comunque visualizzata correttamente in Player.

È possibile che un programma diverso da Windows Media Player possa registrarsi come programma predefinito per l'apertura di file asx. Il modello a oggetti Windows Media Player serie 9 o successive include un nuovo metodo, **openPlayer**, che consente di specificare un Uniform Resource Locator (URL) per il contenuto da riprodurre. Quando si usa il **metodo openPlayer,** Windows Media Player si apre sempre in modalità completa per riprodurre il contenuto specificato. Usando questo metodo, è possibile assicurarsi che il contenuto HTMLView sia visualizzato in Windows Media Player, anziché in un'altra applicazione che ha assunto l'associazione del tipo di file asx.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player.openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




