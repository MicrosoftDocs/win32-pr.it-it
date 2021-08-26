---
description: Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: Metodo ITipAutocompleteClient::AdviseProvider (TipAutoComplete.h)
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
ms.openlocfilehash: dd48cdfbf35c5132b42f8185cdc93f53ec34c77df78a51d16da9fa5a5311c144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938581"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>Metodo ITipAutocompleteClient::AdviseProvider

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

*hWndField* \[ Pollici\]
</dt> <dd>

Handle della finestra del campo che fornisce la funzionalità di completamento automatico.

</dd> <dt>

*pIACProvider* \[ Pollici\]
</dt> <dd>

Puntatore a interfaccia all'interfaccia del provider di completamento automatico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete.h (richiede anche Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**Metodo ITipAutocompleteClient::UnadviseProvider**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Informazioni di riferimento sul pannello di input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




