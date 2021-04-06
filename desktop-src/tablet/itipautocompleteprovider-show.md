---
description: Consente di visualizzare o nascondere l'elenco di completamento automatico.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Metodo ITipAutocompleteProvider:: Show (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759815"
---
# <a name="itipautocompleteprovidershow-method"></a>Metodo ITipAutocompleteProvider:: Show

Consente di visualizzare o nascondere l'elenco di completamento automatico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fShow* \[ in\]
</dt> <dd>

**True** per visualizzare l'interfaccia utente di completamento automatico, **false** per nascondere l'interfaccia utente dell'elenco di completamento automatico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal client per mostrare o nascondere l'elenco di completamento automatico. Se l'elenco di completamento automatico non viene visualizzato e *fShow* è **false**, questo metodo non esegue alcuna operazione. Se viene visualizzato l'elenco di completamento automatico e *fShow* è **true**, questo metodo non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




