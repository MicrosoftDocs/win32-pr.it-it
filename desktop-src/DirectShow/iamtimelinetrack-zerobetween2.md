---
description: 'Il metodo ZeroBetween2 rimuove tutti gli elementi dalla traccia tra le ore specificate. Questo metodo è equivalente a IAMTimelineTrack:: ZeroBetween, ma accetta valori REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'Metodo IAMTimelineTrack:: ZeroBetween2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325615"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>Metodo IAMTimelineTrack:: ZeroBetween2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ZeroBetween2` metodo rimuove tutti gli elementi dalla traccia tra le ore specificate. Questo metodo è equivalente a [**IAMTimelineTrack:: ZeroBetween**](iamtimelinetrack-zerobetween.md), ma accetta valori [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtStart* 
</dt> <dd>

Inizio dell'intervallo da cancellare, in secondi.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Fine dell'intervallo da cancellare, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                             | Descrizione                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | L'intervallo di tempo va oltre tutti gli elementi nella traccia.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                             |



 

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

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




