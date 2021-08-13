---
title: Metodo IBackgroundCopyJob EnumFiles (Deliveryoptimization.h)
description: Recupera un puntatore a interfaccia IEnumBackgroundCopyFiles utilizzato per enumerare i file in un processo.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Metodo EnumFiles
- Metodo EnumFiles, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ecd27e1de8dfaa16d7f5d2dc3218d3c993148a0878976e329b4953cefdc4c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543017"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>Metodo IBackgroundCopyJob::EnumFiles

Recupera un [**puntatore a interfaccia IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) utilizzato per enumerare i file in un processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnumFiles* \[ Cambio\]
</dt> <dd>

[**Puntatore a interfaccia IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) che viene utilizzato per enumerare i file nel processo. Al *termine, rilasciare ppEnumFiles.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo **restituisce** S_OK esito positivo o uno dei valori **HRESULT** COM standard in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob definito come 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





