---
title: Pagine di individuazione
description: Pagine di individuazione
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player Online Stores, pagine di individuazione
- archivi online, pagine di individuazione
- digitare 1 archivi online, pagine di individuazione
- Windows Media Player Library, pagine di individuazione
- raccolta, pagine di individuazione
- pagine di individuazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723518"
---
# <a name="discovery-pages"></a>Pagine di individuazione

Se lo Store online attivo è di tipo 1, Windows Media Player Visualizza il contenuto dell'archivio nella relativa interfaccia utente. Il controllo visualizzazione albero libreria dispone di un nodo per l'archivio online. Quando l'utente fa clic su tale nodo o su uno dei relativi sottonodi, Windows Media Player Visualizza il contenuto del negozio online nel riquadro dei dettagli.

Quando l'utente interagisce con il contenuto dell'archivio online nel controllo di visualizzazione albero o nel riquadro dei dettagli, Windows Media Player Visualizza le pagine Web, denominate *pagine di individuazione*, fornite dallo Store online. Le pagine di individuazione forniscono informazioni aggiuntive sulla musica mentre l'utente Esplora il catalogo del negozio online. Le pagine di individuazione comunicano con Windows Media Player tramite le proprietà, i metodi e gli eventi dell' [oggetto esterno](external-object-for-type-1-online-stores.md).

Ogni volta che Windows Media Player modifica la visualizzazione del contenuto del negozio online, viene chiamato [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate), implementato dal plug-in del negozio online, per ottenere l'URL della pagina di individuazione da visualizzare con la nuova visualizzazione.

La visualizzazione del contenuto del negozio online in Windows Media Player è caratterizzata da cinque informazioni: attività, tipo di posizione, ID posizione, tipo di elemento selezionato e ID elemento selezionato. Windows Media Player fornisce questi cinque elementi al metodo **GetTemplate** nei parametri *Task*, *location*, *pContext*, *clickLocation* e *pClickContext* . Windows Media Player rende questi cinque elementi disponibili per le pagine di individuazione nelle proprietà *Task*, *libraryLocationType*, *libraryLocationID*, *selectedItemType* e *selectedItemID* dell'oggetto **esterno** . Per ulteriori informazioni sul modo in cui Windows Media Player specifica la visualizzazione del contenuto dell'archivio online, vedere [percorso e elemento selezionato](location-and-selected-item.md).

Oltre ad abilitare una pagina di individuazione per la comunicazione con Windows Media Player, l'oggetto **esterno** consente a una pagina di individuazione di comunicare con il plug-in del negozio online. In tal caso, Windows Media Player funge da ponte tra la pagina di individuazione e il plug-in. La pagina di individuazione, ad esempio, può chiamare [External. SendMessage](external-sendmessage.md) per inviare un messaggio personalizzato al plug-in. Windows Media Player riceve questa chiamata al metodo e chiama a sua volta [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) per passare il messaggio al plug-in. Al termine dell'elaborazione del messaggio da parte del plug-in, viene chiamato [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete). Windows Media Player notifica quindi la pagina di individuazione generando l'evento [External. OnSendMessageComplete](external-onsendmessagecomplete-event.md) .

L'oggetto **esterno** fornisce inoltre un modo per la comunicazione di una pagina di individuazione con un'altra pagina di individuazione. Quando uno script in una pagina di individuazione chiama [External. changeView](external-changeview.md), lo script può fornire una stringa nel parametro *ViewParams* . Windows Media Player non interpreta la stringa *ViewParams* , ma rende disponibile la stringa per la pagina di individuazione successiva nella proprietà [External. viewParameters](external-viewparameters.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Posizione e elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 




