---
description: Gestisce il lato dell'applicazione dell'integrazione di completamento automatico del pannello di input di testo.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interfaccia ITipAutocompleteProvider (TipAutoComplete. h)
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
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319160"
---
# <a name="itipautocompleteprovider-interface"></a>Interfaccia ITipAutocompleteProvider

Gestisce il lato dell'applicazione dell'integrazione di completamento automatico del pannello di input di testo.

## <a name="members"></a>Membri

L'interfaccia **ITipAutocompleteProvider** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteProvider** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITipAutocompleteProvider** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Visualizza**](itipautocompleteprovider-show.md)                           | Consente di visualizzare o nascondere l'elenco di completamento automatico.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inchiostrato nel pannello di input.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> </dl>

 

