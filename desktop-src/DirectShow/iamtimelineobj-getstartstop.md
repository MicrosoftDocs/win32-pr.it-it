---
description: Il metodo GetStartStop recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Metodo IAMTimelineObj:: GetStartStop (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327110"
---
# <a name="iamtimelineobjgetstartstop-method"></a>Metodo IAMTimelineObj:: GetStartStop

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetStartStop` metodo recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStart* 
</dt> <dd>

Riceve l'ora di inizio, in unità di 100 nanosecondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Riceve l'ora di arresto, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le composizioni, i gruppi e le tracce hanno sempre l'ora di inizio 0.

Durante il rendering, DES Arrotonda gli orari di inizio e di fine di un oggetto al limite di frame più vicino. Tuttavia, DES non sovrascrive i tempi dell'oggetto. Se si modifica la frequenza dei fotogrammi del gruppo, i tempi arrotondati vengono sempre calcolati a partire dai tempi originali. Per altre informazioni, [ora in servizi di modifica DirectShow](time-in-directshow-editing-services.md).

Per determinare le ore di inizio e di fine nel progetto di cui è stato eseguito il rendering, passare i valori restituiti da `GetStartStop` al metodo [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) .

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

 

 




