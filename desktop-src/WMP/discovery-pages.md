---
title: Pagine di individuazione
description: Pagine di individuazione
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player online, pagine di individuazione
- negozi online, pagine di individuazione
- tipo 1 negozi online, pagine di individuazione
- Windows Media Player, pagine di individuazione
- libreria, pagine di individuazione
- pagine di individuazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe29ed5d3948bbdcd6f36239938e3a4e552362318b6ec48658e85895cb58d163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997341"
---
# <a name="discovery-pages"></a>Pagine di individuazione

Se lo store online attivo è di tipo 1, Windows Media Player il contenuto del negozio nell'interfaccia utente. Il controllo visualizzazione albero della libreria include un nodo per il negozio online. Quando l'utente fa clic su tale nodo o su uno dei relativi sottonodi, Windows Media Player il contenuto dello store online nel riquadro dei dettagli.

Quando l'utente interagisce con il contenuto del negozio online nel controllo di visualizzazione albero o nel riquadro dei dettagli, Windows Media Player visualizza le pagine Web, denominate pagine di individuazione, fornite dallo store online. Le pagine di individuazione forniscono informazioni aggiuntive sulla musica mentre l'utente esplora il catalogo del negozio online. Le pagine di individuazione comunicano con Windows Media Player tramite le proprietà, i metodi e gli eventi [dell'oggetto esterno](external-object-for-type-1-online-stores.md).

Ogni volta che Windows Media Player modifica la visualizzazione del contenuto dello store online, chiama [IWMPContentPartner::GetTemplate,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)implementato dal plug-in dello store online, per ottenere l'URL della pagina di individuazione da visualizzare con la nuova visualizzazione.

La visualizzazione del contenuto dello store online in Windows Media Player è caratterizzata da cinque informazioni: attività, tipo di posizione, ID posizione, tipo di elemento selezionato e ID elemento selezionato. Windows Media Player fornisce questi cinque elementi al metodo **GetTemplate** nei parametri *task*, *location*, *pContext*, *clickLocation* *e pClickContext.* Windows Media Player rende questi cinque elementi disponibili per le pagine di individuazione nelle proprietà task *,* *libraryLocationType*, *libraryLocationID*, *selectedItemType* e *selectedItemID* dell'oggetto **External.** Per altre informazioni su come Windows Media Player specifica la visualizzazione del contenuto dello store online, vedere [Posizione e elemento selezionato.](location-and-selected-item.md)

Oltre a consentire a una pagina di individuazione  di comunicare con Windows Media Player, l'oggetto External consente a una pagina di individuazione di comunicare con il plug-in dello store online. In questo caso, Windows Media Player funge da ponte tra la pagina di individuazione e il plug-in. Ad esempio, la pagina di individuazione può [chiamare External.sendMessage](external-sendmessage.md) per inviare un messaggio personalizzato al plug-in. Windows Media Player riceve questa chiamata al metodo e a sua volta chiama [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) per passare il messaggio al plug-in. Al termine dell'elaborazione del messaggio, il plug-in chiama [IWMPContentPartnerCallback::SendMessageComplete.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) Windows Media Player quindi invia una notifica alla pagina di individuazione generando [l'evento External.OnSendMessageComplete.](external-onsendmessagecomplete-event.md)

**L'oggetto** esterno consente inoltre a una pagina di individuazione di comunicare con un'altra pagina di individuazione. Quando lo script in una pagina di individuazione [chiama External.changeView,](external-changeview.md)lo script può fornire una stringa nel *parametro ViewParams.* Windows Media Player non interpreta la stringa *ViewParams,* ma la rende disponibile per la pagina di individuazione successiva nella [proprietà External.viewParameters.](external-viewparameters.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Posizione ed elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 




