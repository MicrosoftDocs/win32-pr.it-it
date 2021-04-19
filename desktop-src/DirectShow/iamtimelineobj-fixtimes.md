---
description: Il metodo FixTimes Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Metodo IAMTimelineObj:: FixTimes (qedit. h)'
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
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333592"
---
# <a name="iamtimelineobjfixtimes-method"></a>Metodo IAMTimelineObj:: FixTimes

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `FixTimes` Metodo Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FixTimes(
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

Restituisce \_ OK se ha esito positivo o E \_ NOTINTREE se l'oggetto non fa parte di un gruppo.

## <a name="remarks"></a>Commenti

Durante il rendering, DES Arrotonda gli orari di inizio e di fine dell'oggetto al limite del frame più vicino. Tuttavia, DES non sovrascrive i tempi dell'oggetto. Se si modifica la frequenza dei fotogrammi del gruppo, i tempi arrotondati vengono sempre calcolati a partire dai tempi originali. Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).

Utilizzare questo metodo per determinare gli orari di inizio e di fine accurati nel progetto sottoposto a rendering. Ad esempio, è consigliabile cercare l'ora arrotondata, anziché l'ora di inizio e di fine dell'oggetto. Chiamare [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md) per ottenere l'ora originale e passare tali valori a `FixTimes` .

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




