---
description: Il metodo FixMediaTimes arrotonda i valori di tempo specificati al limite del frame più vicino, come definito dalla frequenza fotogrammi di output. In generale, le applicazioni non devono chiamare questo metodo.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: Metodo IAMTimelineSrc::FixMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dcace4e501a27b1f82b148533f382f5c86bafb17d9bf34343f1e43a8893672c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052401"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>Metodo IAMTimelineSrc::FixMediaTimes

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo arrotonda i valori di tempo specificati al limite del frame più `FixMediaTimes` vicino, come definito dalla frequenza fotogrammi di output. In generale, le applicazioni non devono chiamare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di inizio, in unità da 100 nanosecondi. Se la chiamata ha esito positivo, questa variabile viene impostata sull'ora arrotondata.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che contiene il tempo di arresto, in unità di 100 nanosecondi. Se la chiamata ha esito positivo, questa variabile viene impostata sull'ora arrotondata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo è simile al metodo [**IAMTimelineObj::FixTimes,**](iamtimelineobj-fixtimes.md) ma mantiene il rapporto originale tra i tempi dei supporti e della sequenza temporale. L'arrotondamento dei tempi al limite del fotogramma più vicino potrebbe distorcere questo rapporto.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




