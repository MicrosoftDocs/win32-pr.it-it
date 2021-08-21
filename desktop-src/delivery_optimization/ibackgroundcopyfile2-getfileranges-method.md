---
title: Metodo IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization.h)
description: Recupera gli intervalli da scaricare dal file remoto.
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
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047079"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>Metodo IBackgroundCopyFile2::GetFileRanges

Recupera gli intervalli da scaricare dal file remoto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RangeCount* \[ in, out\]
</dt> <dd>

Numero di elementi in *Ranges*.

</dd> <dt>

*Intervalli* \[ Cambio\]
</dt> <dd>

Matrice di [**BG_FILE_RANGE**](bg-file-range.md) che specificano gli intervalli da scaricare. Al termine, chiamare la [**funzione CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *Ranges*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti seguenti, nonché altri.



| Codice restituito                                                                              | Descrizione                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Operazione riuscita<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Non è stato specificato alcun intervallo oppure il processo è un processo di caricamento o caricamento-risposta. *RangeCount* è impostato su zero e *Ranges* è impostato su **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 definito come 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

