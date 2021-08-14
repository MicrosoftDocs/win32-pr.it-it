---
description: Il metodo FixTimes2 arrotonda gli orari di inizio e di arresto specificati ai limiti del frame più vicini, come definito dall'impostazione della frequenza fotogrammi del gruppo padre. Questo metodo equivale a IAMTimelineObj::FixTimes, ma accetta valori REFTIME.
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: Metodo IAMTimelineObj::FixTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74890c2b094172ac3ced0c9fd192a755d051b56df22301b4d64d9003eaa74e9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400906"
---
# <a name="iamtimelineobjfixtimes2-method"></a>Metodo IAMTimelineObj::FixTimes2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il metodo arrotonda i tempi di inizio e di arresto specificati ai limiti del frame più vicini, come definito `FixTimes2` dall'impostazione della frequenza fotogrammi del gruppo padre. Questo metodo equivale a [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixTimes2(
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

Puntatore a una variabile che contiene il tempo di arresto, espresso in secondi. Se la chiamata ha esito positivo, questa variabile viene impostata sull'ora arrotondata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure E \_ NOTINTREE se l'oggetto non fa parte di un gruppo.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




