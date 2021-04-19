---
description: Il metodo ModifyStopTime imposta l'ora di arresto, relativa alla sequenza temporale.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'Metodo IAMTimelineSrc:: ModifyStopTime (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332750"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>Metodo IAMTimelineSrc:: ModifyStopTime

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ModifyStopTime` metodo imposta l'ora di arresto, relativa alla sequenza temporale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stop* 
</dt> <dd>

Nuova ora di arresto, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ INVALIDARG se l'ora specificata non è valida.

## <a name="remarks"></a>Commenti

Questo metodo equivale a chiamare [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) con l'ora di inizio originale e una nuova ora di arresto.

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

 

 




