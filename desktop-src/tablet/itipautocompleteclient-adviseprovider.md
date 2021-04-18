---
description: Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Metodo ITipAutocompleteClient:: AdviseProvider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313454"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>Metodo ITipAutocompleteClient:: AdviseProvider

Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWndField* \[ in\]
</dt> <dd>

Handle della finestra del campo che fornisce la funzionalità di completamento automatico.

</dd> <dt>

*pIACProvider* \[ in\]
</dt> <dd>

Puntatore di interfaccia all'interfaccia del provider di completamento automatico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**Metodo ITipAutocompleteClient:: UnadviseProvider**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




