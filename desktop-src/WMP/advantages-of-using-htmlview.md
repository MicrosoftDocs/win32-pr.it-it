---
title: Vantaggi dell'uso di HTMLView
description: Vantaggi dell'uso di HTMLView
ms.assetid: bbec9471-87f1-4c41-a322-f11e9e1dec37
keywords:
- Playlist Windows Media Metafile, vantaggi HTMLView
- playlist, vantaggi di HTMLView
- playlist di metafile, vantaggi HTMLView
- Playlist Windows Media Metafile, vantaggi di HTMLView
- playlist, vantaggi di HTMLView
- playlist di metafile, vantaggi di HTMLView
- vantaggi di HTMLView
- Windows Media Player, vantaggi di HTMLView
- Windows Media Player, vantaggi HTMLView
- HTMLView, vantaggi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5e5409db969f5e9a8e0df18738f4995490b1d83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396419"
---
# <a name="advantages-of-using-htmlview"></a>Vantaggi dell'uso di HTMLView

La funzionalità HTMLView consente di creare in modo semplice un'esperienza utente integrata basata sul Web che riproduce contenuti multimediali digitali utilizzando l'aspetto familiare del Web. Quando si combinano contenuti basati sul Web con contenuto multimediale digitale nell'interfaccia utente di Windows Media Player, il risultato può avere un maggiore effetto sull'utente rispetto a quando gli elementi vengono visualizzati separatamente. Il contenuto multimediale digitale è migliorato da informazioni correlate interessanti, mentre la pagina Web può fornire collegamenti a contenuti simili, creando così nuove opportunità di business.

## <a name="htmlview-provides-a-better-user-experience"></a>HTMLView offre un'esperienza utente migliore

Gli utenti desiderano e accedono alle informazioni che possono essere offerte con contenuto multimediale digitale, ma non vogliono gestire una serie apparentemente infinita di annunci popup. L'uso di finestre del browser popup per visualizzare la pubblicità sul Web è diventato così comune che è ora disponibile un software che impedisce l'apertura di tali finestre. Questo software può avere l'effetto collaterale indesiderato di impedire la visualizzazione di pagine Web legittime, a volte l'eliminazione di un'intera presentazione multimediale digitale.

Quando si usa la funzionalità HTMLView, gli utenti non devono più gestire le finestre popup. Invece di aprire una finestra separata del browser per fornire informazioni aggiuntive all'utente, è possibile visualizzare contenuto personalizzato basato sul Web nella funzionalità **ora di riproduzione** dell'interfaccia utente di Windows Media Player mentre il lettore riproduce il contenuto audio o video desiderato dall'utente. Gli utenti possono controllare la riproduzione usando i controlli Media Player di Windows. Poiché il contenuto viene riprodotto nel lettore in modalità completa, il software progettato per impedire gli annunci popup non impedisce agli utenti di apprezzare il contenuto.

## <a name="htmlview-content-is-easy-to-create"></a>Il contenuto di HTMLView è facile da creare

Come suggerisce il nome della funzionalità, è possibile creare contenuto basato sul Web con la funzionalità HTMLView usando Hypertext Markup Language (HTML). Se è già stato creato contenuto per il Web, questo significa che non è necessario imparare un nuovo linguaggio di programmazione per creare facilmente contenuti avanzati con la funzionalità HTMLView. Se sono già presenti pagine Web con un controllo ActiveX Windows Media Player incorporato, è possibile visualizzare queste pagine nell'interfaccia utente del lettore semplicemente puntando a queste pagine Web da un metafile di Windows Media (file con estensione asx) usando un parametro speciale.

Windows Media Player utilizza un'istanza incorporata di Microsoft Internet Explorer per visualizzare il contenuto di HTMLView. Ciò significa che non è necessario prendere in considerazione diversi browser Internet, più modelli di scripting o diversi linguaggi di scripting durante la creazione di pagine Web. Anche se l'utente non usa Internet Explorer come browser predefinito, la pagina Web viene ancora visualizzata correttamente nel lettore.

È possibile che un programma diverso da Windows Media Player possa registrarsi come programma predefinito per l'apertura di file con estensione asx. Il modello a oggetti di Windows Media Player 9 o versione successiva include un nuovo metodo, **openPlayer**, che consente di specificare un Uniform Resource Locator (URL) per il contenuto che si desidera riprodurre. Quando si usa il metodo **openPlayer** , Windows Media Player viene sempre aperto in modalità completa per riprodurre il contenuto specificato. Utilizzando questo metodo, è possibile verificare che il contenuto di HTMLView venga visualizzato in Windows Media Player, anziché in un'altra applicazione che ha assunto l'associazione del tipo di file. asx.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Player. openPlayer**](player-openplayer.md)
</dt> </dl>

 

 




