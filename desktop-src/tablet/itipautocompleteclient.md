---
description: Consente al client di chiamare l'oggetto provider di completamento automatico del pannello di input di testo dell'applicazione.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interfaccia ITipAutocompleteClient (TipAutoComplete. h)
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
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318705"
---
# <a name="itipautocompleteclient-interface"></a>Interfaccia ITipAutocompleteClient

Consente al client di chiamare l'oggetto provider di completamento automatico del pannello di input di testo dell'applicazione.

## <a name="members"></a>Membri

L'interfaccia **ITipAutocompleteClient** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteClient** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITipAutocompleteClient** dispone di questi metodi.



| Metodo                                                              | Descrizione                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare la sovrapposizione del pannello di input.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Determina se il pannello di input è pronto per visualizzare l'elenco di completamento automatico.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Annulla la registrazione del provider associato.<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e per rimuovere tutto il testo rimanente che non è ancora stato inserito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

