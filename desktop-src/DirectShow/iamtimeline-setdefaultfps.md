---
description: Il metodo SetDefaultFPS imposta la frequenza dei fotogrammi di output predefinita, in fotogrammi al secondo. I gruppi usano questo valore come frequenza dei fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo IAMTimelineGroup::SetOutputFPS sul gruppo.
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: Metodo IAMTimeline::SetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d98b4ea7a69f527f0a79ddbe559d3602afecd06e4728da23ef3627ed7a313a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052811"
---
# <a name="iamtimelinesetdefaultfps-method"></a>Metodo IAMTimeline::SetDefaultFPS

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetDefaultFPS` metodo imposta la frequenza dei fotogrammi di output predefinita, in fotogrammi al secondo. I gruppi usano questo valore come frequenza dei fotogrammi predefinita. Per impostare la frequenza dei fotogrammi di un gruppo, chiamare il metodo [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) sul gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FPS* 
</dt> <dd>

Frequenza dei fotogrammi predefinita, in fotogrammi al secondo.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




