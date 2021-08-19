---
description: Callback che notifica all'host il numero di thread e gruppi del compute shader nella richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPipeLineStagesCallback2::ThreadDataDimensionCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0d56989325aa59f4bc1681e3d799420453945e7363736410ba5e46efbc69c3f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023041"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>Metodo IPipeLineStagesCallback2::ThreadDataDimensionCallback

Callback che notifica all'host il numero di thread e gruppi del compute shader nella richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a>Parametri

*threadGroupCount*   
Conteggio multidimensionale dei gruppi di thread.

*threadGroupSize*   
Dimensione multidimensionale di ogni gruppo di thread.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPipeLineStagesCallback2**](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
