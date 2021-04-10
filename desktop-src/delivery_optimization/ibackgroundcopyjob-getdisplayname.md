---
title: Metodo GetDisplayName di metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera il nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (metodo)
- Metodo GetDisplayName, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, Metodo GetDisplayName
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964700"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>Metodo metodo ibackgroundcopyjob:: GetDisplayName

Recupera il nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDisplayName* \[ out\]
</dt> <dd>

Stringa con terminazione null che contiene il nome visualizzato che identifica il processo. Più di un processo può avere lo stesso nome visualizzato. Chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *ppDisplayName* al termine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                                  | Descrizione                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | Il nome visualizzato è stato recuperato.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Il parametro *ppDisplayName* non può essere **null**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

