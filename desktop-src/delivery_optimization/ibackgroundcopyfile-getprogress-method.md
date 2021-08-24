---
title: Metodo GetProgress IBackgroundCopyFile (Deliveryoptimization.h)
description: Recupera informazioni sullo stato di avanzamento del trasferimento di file.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Metodo GetProgress
- Metodo GetProgress, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, metodo GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7c5fe4a9fcfac86403fd7f4c330d437156e57179b3bf692f53bf3777399b9bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610501"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>Metodo IBackgroundCopyFile::GetProgress

Recupera informazioni sullo stato di avanzamento del trasferimento di file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProgress* \[ Cambio\]
</dt> <dd>

Struttura i cui membri indicano lo stato di avanzamento del trasferimento di file. Per informazioni dettagliate sul tipo di informazioni sullo stato disponibili, vedere la [**BG_FILE_PROGRESS**](bg-file-progress.md) di stato.

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
| IID<br/>                      | IID_IBackgroundCopyFile definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyJob::GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





