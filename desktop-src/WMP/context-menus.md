---
title: Menu di scelta rapida
description: Menu di scelta rapida
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player online, menu di scelta rapida
- negozi online, menu di scelta rapida
- tipo 1 punti vendita online, menu di scelta rapida
- Windows Media Player online, menu di scelta rapida personalizzati
- online store, menu di scelta rapida personalizzati
- tipo 1 punti vendita online, menu di scelta rapida personalizzati
- menu di scelta rapida
- menu di scelta rapida personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ad3bba5863f83b5f324821ec0904e7ef4c5881c7f10b9214eebde1081b217d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119350"
---
# <a name="context-menus"></a>Menu di scelta rapida

I negozi online possono fornire menu di scelta rapida personalizzati. A tale scopo, il plug-in dello store online implementa il [metodo IWMPContentPartner::GetCommands.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) Windows Media Player chiama questo metodo per fornire informazioni sulla posizione nell'interfaccia utente in cui viene visualizzato il menu di scelta rapida (in cui l'utente ha fatto clic con il pulsante destro del mouse). Il plug-in restituisce una matrice di [strutture WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) che descrivono ogni voce di menu di scelta rapida, incluso un ID comando per ognuna.

Dopo Windows Media Player ha recuperato la matrice, player usa la matrice per compilare il menu di scelta rapida visualizzato dall'utente. Quando l'utente fa clic su una voce nel menu di scelta rapida, il lettore chiama [IWMPContentPartner::InvokeCommand,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)passando l'ID comando associato alla voce di menu tramite il *parametro dwCommandID.* Il lettore passa anche un valore di posizione della libreria e una matrice di ID che rappresenta le voci su cui è stato richiamato il menu, ad esempio una matrice di ID traccia. Usando queste informazioni, il plug-in può avviare qualsiasi processo appropriato in risposta al clic del mouse dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




