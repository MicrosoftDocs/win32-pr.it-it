---
description: Il metodo ModifyStopTime imposta l'ora di arresto relativa alla sequenza temporale.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: Metodo IAMTimelineSrc::ModifyStopTime (Qedit.h)
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
ms.openlocfilehash: f6d611395ad8989ea551fb98d1a3d538786881b0a5afc908a030367cac52ee80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952820"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>Metodo IAMTimelineSrc::ModifyStopTime

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

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

Nuovo tempo di arresto, in unità da 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ INVALIDARG se l'ora specificata non è valida.

## <a name="remarks"></a>Commenti

Questo metodo equivale a chiamare [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) con l'ora di inizio originale e una nuova ora di arresto.

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

 

 




