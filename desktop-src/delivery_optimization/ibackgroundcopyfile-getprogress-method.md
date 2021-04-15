---
title: Metodo getProgress IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera le informazioni sullo stato di avanzamento del trasferimento di file.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Metodo getProgress
- Metodo getProgress, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, metodo getProgress
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
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476373"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>Metodo IBackgroundCopyFile:: getProgress

Recupera le informazioni sullo stato di avanzamento del trasferimento di file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProgress* \[ out\]
</dt> <dd>

Struttura i cui membri indicano lo stato di avanzamento del trasferimento di file. Per informazioni dettagliate sul tipo di informazioni sullo stato di avanzamento disponibili, vedere la struttura [**BG_FILE_PROGRESS**](bg-file-progress.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: getProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





