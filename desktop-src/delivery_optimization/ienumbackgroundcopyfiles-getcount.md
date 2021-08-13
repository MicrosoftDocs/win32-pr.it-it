---
title: Metodo GetCount IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Recupera un conteggio del numero di file nell'enumerazione .
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount (metodo)
- Metodo GetCount, interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, metodo GetCount
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67ee932079a7c67619fe769cbe5d1b6705261655853f1adccb14bf5d12eecf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409911"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>Metodo IEnumBackgroundCopyFiles::GetCount

Recupera un conteggio del numero di file nell'enumerazione .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCount* \[ Cambio\]
</dt> <dd>

Numero di file nell'enumerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo **restituisce** S_OK in caso di esito positivo o uno dei valori **HRESULT** COM standard in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles è definito come CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





