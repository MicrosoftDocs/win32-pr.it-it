---
description: Consente al client di chiamare l'oggetto provider di completamento automatico del Pannello input di testo dell'applicazione.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interfaccia ITipAutocompleteClient (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: dac9b1a6c581be8a8fb19df4f812a5866403d949d19739bb8ae99a0fffbe5e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590291"
---
# <a name="itipautocompleteclient-interface"></a>Interfaccia ITipAutocompleteClient

Consente al client di chiamare l'oggetto provider di completamento automatico del Pannello input di testo dell'applicazione.

## <a name="members"></a>Membri

**L'interfaccia ITipAutocompleteClient** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteClient** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ITipAutocompleteClient.**



| Metodo                                                              | Descrizione                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare di sovrapporsi al Pannello input penna.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Determina se il Pannello input penna è pronto per visualizzare l'elenco di completamento automatico.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Annulla la registrazione del provider associato.<br/>                                                                                                                      |
| [**Selezione utente**](itipautocompleteclient-userselection.md)       | Notifica al Pannello input penna che l'utente ha selezionato un elemento nell'elenco di completamento automatico e rimuove tutto il testo rimanente che non è ancora stato inserito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete.h (richiede anche Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

