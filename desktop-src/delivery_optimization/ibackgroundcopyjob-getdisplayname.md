---
title: Metodo IBackgroundCopyJob GetDisplayName (Deliveryoptimization.h)
description: Recupera il nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (metodo)
- Metodo GetDisplayName, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetDisplayName
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
ms.openlocfilehash: 1a50d2bdc1c492725b79368774f07755c7b629d73209a7d53f865cc738eb7025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755541"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>Metodo IBackgroundCopyJob::GetDisplayName

Recupera il nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDisplayName* \[ Cambio\]
</dt> <dd>

Stringa con terminazione Null contenente il nome visualizzato che identifica il processo. Più processi possono avere lo stesso nome visualizzato. Al [**termine, chiamare la funzione CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per *liberare ppDisplayName.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                                  | Descrizione                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>     | Il nome visualizzato è stato recuperato correttamente.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Il *parametro ppDisplayName* non può essere **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob è definito come 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

