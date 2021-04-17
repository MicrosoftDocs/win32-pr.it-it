---
title: Metodo Suspend metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Sospende un processo. I nuovi processi, i processi in errore e i processi che hanno terminato il trasferimento dei file vengono sospesi automaticamente.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Metodo Suspend
- Metodo Suspend, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400622"
---
# <a name="ibackgroundcopyjobsuspend-method"></a>Metodo metodo ibackgroundcopyjob:: Suspend

Sospende un processo. I nuovi processi, i processi in errore e i processi che hanno terminato il trasferimento dei file vengono sospesi automaticamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Suspend();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                                          | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Il processo è stato sospeso.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

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
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





