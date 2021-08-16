---
title: Metodo GetError IBackgroundCopyError (Deliveryoptimization.h)
description: Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Metodo GetError
- Metodo GetError, interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, metodo GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d147bc877f9694617ec94651f53f4cf438c00de8d752710c3659f24ba4ffe21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810327"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>Metodo IBackgroundCopyError::GetError

Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Oggetto pContext* \[ Cambio\]
</dt> <dd>

Contesto in cui si è verificato l'errore. Per un elenco di valori di contesto, vedere [**l'BG_ERROR_CONTEXT**](bg-error-context.md) di contesto.

</dd> <dt>

*pErrorCode* \[ Cambio\]
</dt> <dd>

Codice di errore dell'errore che si è verificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo **restituisce** S_OK in caso di esito positivo o uno dei valori HRESULT COM standard in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError è definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





