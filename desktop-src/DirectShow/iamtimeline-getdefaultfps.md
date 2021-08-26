---
description: Il metodo GetDefaultFPS recupera la frequenza fotogrammi di output predefinita, in fotogrammi al secondo (FPS). I gruppi usano questo valore come frequenza fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo IAMTimelineGroup::SetOutputFPS nel gruppo.
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: Metodo IAMTimeline::GetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 38f12abe47829544453d0aed9b8f08bffd2b5864f78fc35c873622d960387931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107851"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Metodo IAMTimeline::GetDefaultFPS

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetDefaultFPS` metodo recupera la frequenza fotogrammi di output predefinita, in fotogrammi al secondo (FPS). I gruppi usano questo valore come frequenza fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) nel gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFPS* 
</dt> <dd>

Riceve la frequenza fotogrammi predefinita, in fotogrammi al secondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




