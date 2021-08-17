---
description: Il metodo FixMediaTimes2 arrotonda i valori di tempo specificati al limite del frame più vicino, come definito dalla frequenza dei fotogrammi di output. Questo metodo è equivalente a IAMTimelineSrc::FixMediaTimes, ma accetta valori REFTIME.
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: Metodo IAMTimelineSrc::FixMediaTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ceff01e17d82ed59e8d63811841e58e97323a9be4ec4c40b719bb655aac464e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399621"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a>Metodo IAMTimelineSrc::FixMediaTimes2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `FixMediaTimes2` metodo arrotonda i valori di tempo specificati al limite del fotogramma più vicino, come definito dalla frequenza dei fotogrammi di output. Questo metodo è equivalente a [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di inizio, in secondi. Se la chiamata ha esito positivo, questa variabile viene impostata sull'ora arrotondata.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di arresto, in secondi. Se la chiamata ha esito positivo, questa variabile viene impostata sull'ora arrotondata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




