---
title: Menu di scelta rapida
description: Menu di scelta rapida
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player Online Store, menu di scelta rapida
- archivi online, menu di scelta rapida
- digitare 1 archivi online, menu di scelta rapida
- Windows Media Player Online Stores, menu di scelta rapida personalizzati
- negozi online, menu di scelta rapida personalizzati
- digitare 1 archivi online, menu di scelta rapida personalizzati
- menu di scelta rapida
- menu di scelta rapida personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398542"
---
# <a name="context-menus"></a>Menu di scelta rapida

Gli archivi online possono fornire menu di scelta rapida personalizzati. A tale scopo, il plug-in di archivio online implementa il metodo [IWMPContentPartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) . Windows Media Player chiama questo metodo per fornire informazioni sul percorso nell'interfaccia utente in cui viene visualizzato il menu di scelta rapida (in cui l'utente ha fatto clic con il pulsante destro del mouse). Il plug-in restituisce una matrice di strutture [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) che descrivono ogni voce di menu di scelta rapida, incluso un ID di comando per ognuno di essi.

Dopo che Windows Media Player ha recuperato la matrice, il giocatore usa la matrice per compilare il menu di scelta rapida visualizzato dall'utente. Quando l'utente fa clic su un elemento nel menu di scelta rapida, il lettore chiama [IWMPContentPartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passando l'ID di comando associato alla voce di menu tramite il parametro *dwCommandID* . Il lettore passa anche un valore del percorso della libreria e una matrice di ID che rappresenta gli elementi su cui è stato richiamato il menu, ad esempio una matrice di ID di traccia. Utilizzando queste informazioni, il plug-in può avviare qualsiasi processo appropriato in risposta al clic del mouse dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




