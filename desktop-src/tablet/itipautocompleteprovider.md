---
description: Gestisce il lato dell'applicazione dell'integrazione del completamento automatico del Pannello input di testo.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interfaccia ITipAutocompleteProvider (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 66c1e38c419e7eb37745864b447249d55b384b6c832293bd3fab4d0cc171e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031869"
---
# <a name="itipautocompleteprovider-interface"></a>Interfaccia ITipAutocompleteProvider

Gestisce il lato dell'applicazione dell'integrazione del completamento automatico del Pannello input di testo.

## <a name="members"></a>Membri

**L'interfaccia ITipAutocompleteProvider** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteProvider** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ITipAutocompleteProvider.**



| Metodo                                                                  | Descrizione                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Visualizza**](itipautocompleteprovider-show.md)                           | Visualizza o nasconde l'elenco di completamento automatico.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inserito nel Pannello input penna.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete.h (richiede anche Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento sul pannello di input di testo](text-input-panel-reference.md)
</dt> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> </dl>

 

