---
title: Metodo GetError IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Metodo GetError
- Metodo GetError, interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, metodo getError
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
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964129"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>Metodo IBackgroundCopyError:: GetError

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

*pContext* \[ out\]
</dt> <dd>

Contesto in cui si è verificato l'errore. Per un elenco di valori di contesto, vedere l'enumerazione [**BG_ERROR_CONTEXT**](bg-error-context.md) .

</dd> <dt>

*pErrorCode* \[ out\]
</dt> <dd>

Codice di errore dell'errore che si è verificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S_OK** in esito positivo o uno dei valori HRESULT COM standard in errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError viene definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





