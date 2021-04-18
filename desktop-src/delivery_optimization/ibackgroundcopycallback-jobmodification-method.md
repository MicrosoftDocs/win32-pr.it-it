---
title: Metodo IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobModification quando il processo è stato modificato.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Metodo JobModification
- Metodo JobModification, interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, metodo JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301488"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>Metodo IBackgroundCopyCallback:: JobModification

Ottimizzazione recapito chiama l'implementazione del metodo [**JobModification**](https://www.bing.com/search?q=**JobModification**) quando il processo è stato modificato. Il servizio genera questo evento quando vengono trasferiti i byte, i file sono stati aggiunti al processo, le proprietà sono state modificate o lo stato del processo è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJob* \[ in\]
</dt> <dd>

Contiene i metodi per accedere alle informazioni sulla proprietà, sullo stato di avanzamento e sullo stato del processo. Non rilasciare *pJob*; Rilascia l'interfaccia quando il metodo [**JobModification**](https://www.bing.com/search?q=**JobModification**) restituisce.

</dd> <dt>

*dwReserved* \[ in\]
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve restituire S_OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback viene definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





