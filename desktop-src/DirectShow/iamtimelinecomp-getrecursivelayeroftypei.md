---
description: 'Non supportata. Chiamare invece il metodo IAMTimelineComp:: GetRecursiveLayerOfType.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Metodo IAMTimelineComp:: GetRecursiveLayerOfTypeI (qedit. h)'
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
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326628"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>Metodo IAMTimelineComp:: GetRecursiveLayerOfTypeI

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Non supportata. Chiamare invece il metodo [**IAMTimelineComp:: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) .

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

[**Interfaccia IAMTimelineComp**](iamtimelinecomp.md)
</dt> </dl>

 

 




