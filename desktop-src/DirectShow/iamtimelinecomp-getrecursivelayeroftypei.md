---
description: Non supportata. Chiamare invece il metodo IAMTimelineComp::GetRecursiveLayerOfType.
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: Metodo IAMTimelineComp::GetRecursiveLayerOfTypeI (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc62c0813aa38af450e2f5351390ec958dddd533cc203f52b3bfb70ff45344b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756421"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>Metodo IAMTimelineComp::GetRecursiveLayerOfTypeI

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Non supportata. Chiamare invece [**il metodo IAMTimelineComp::GetRecursiveLayerOfType.**](iamtimelinecomp-getrecursivelayeroftype.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppVirtualTrack* 
</dt> <dd>

Riservato.

</dd> <dt>

*pWhichLayer* 
</dt> <dd>

Riservato.

</dd> <dt>

*Tipo* 
</dt> <dd>

Riservato.

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

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> </dl>

 

 




