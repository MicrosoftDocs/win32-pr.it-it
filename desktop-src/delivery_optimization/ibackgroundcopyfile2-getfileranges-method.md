---
title: Metodo IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
description: Recupera gli intervalli che si desidera scaricare dal file remoto.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Metodo GetFileRanges
- Metodo GetFileRanges, interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, metodo GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400551"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>Metodo IBackgroundCopyFile2:: GetFileRanges

Recupera gli intervalli che si desidera scaricare dal file remoto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RangeCount* \[ in uscita\]
</dt> <dd>

Numero di elementi negli *intervalli*.

</dd> <dt>

*Intervalli* \[ out\]
</dt> <dd>

Matrice di strutture di [**BG_FILE_RANGE**](bg-file-range.md) che specificano gli intervalli da scaricare. Al termine, chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare gli *intervalli*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti seguenti e altri.



| Codice restituito                                                                              | Descrizione                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Operazione riuscita<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Non è stato specificato alcun intervallo oppure il processo è un processo di caricamento o di caricamento-risposta. *RangeCount* è impostato su zero e l' *intervallo* è impostato su **null**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 viene definito come 83e81b93-0873-474d-8A8C-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

