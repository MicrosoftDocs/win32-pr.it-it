---
description: "Il metodo GetStartStop2 recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto. Questo metodo è equivalente a IAMTimelineObj:: GetStartStop, ma accetta valori REFTIME."
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Metodo IAMTimelineObj:: GetStartStop2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327108"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>Metodo IAMTimelineObj:: GetStartStop2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetStartStop2` metodo recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto. Questo metodo è equivalente a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md), ma accetta valori [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStart* 
</dt> <dd>

Riceve l'ora di inizio, in secondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Riceve l'ora di arresto, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

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

 

 




