---
description: Il metodo FixTimes arrotonda gli orari di inizio e di arresto specificati ai limiti del frame più vicini, come definito dall'impostazione della frequenza fotogrammi del gruppo padre.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: Metodo IAMTimelineObj::FixTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6578b18e98c99b471097c98e9dd75de1cdce0c134635cad1fb17e32340eb1a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428421"
---
# <a name="iamtimelineobjfixtimes-method"></a>Metodo IAMTimelineObj::FixTimes

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il metodo arrotonda i tempi di inizio e di arresto specificati ai limiti del frame più vicini, come definito `FixTimes` dall'impostazione della frequenza fotogrammi del gruppo padre.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixTimes(
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

Restituisce S \_ OK in caso di esito positivo oppure E \_ NOTINTREE se l'oggetto non fa parte di un gruppo.

## <a name="remarks"></a>Commenti

Durante il rendering, DES arrotonda i tempi di inizio e di arresto dell'oggetto al limite del frame più vicino. Des, tuttavia, non sovrascrive gli orari dell'oggetto. Se si modifica la frequenza fotogrammi del gruppo, gli orari arrotondati vengono sempre calcolati a partire dall'ora originale. Per altre informazioni, vedere [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Usare questo metodo per determinare tempi di avvio e arresto accurati nel progetto sottoposto a rendering. Ad esempio, è consigliabile cercare gli orari arrotondati, anziché i tempi di inizio e di arresto originali dell'oggetto. Chiamare [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) per ottenere gli orari originali e passare tali valori a `FixTimes` .

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




