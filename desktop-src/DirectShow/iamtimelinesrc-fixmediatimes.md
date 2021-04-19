---
description: Il metodo FixMediaTimes arrotonda i valori temporali specificati al limite del frame più vicino, in base a quanto definito dalla frequenza dei fotogrammi di output. In generale, le applicazioni non devono chiamare questo metodo.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Metodo IAMTimelineSrc:: FixMediaTimes (qedit. h)'
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
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324263"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>Metodo IAMTimelineSrc:: FixMediaTimes

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `FixMediaTimes` Metodo arrotonda i valori temporali specificati al limite del frame più vicino, in base a quanto definito dalla frequenza dei fotogrammi di output. In generale, le applicazioni non devono chiamare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStart* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di inizio, in unità di 100 nanosecondi. Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di arresto, in unità di 100 nanosecondi. Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo è simile al metodo [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) , ma conserva il rapporto originale tra tempi di supporto e tempi di sequenza temporale. L'arrotondamento dei tempi al limite del frame più vicino potrebbe causare la distorsione del rapporto.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




