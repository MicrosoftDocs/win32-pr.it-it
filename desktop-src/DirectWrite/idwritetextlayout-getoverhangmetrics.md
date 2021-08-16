---
title: Metodo IDWriteTextLayout GetOverhangMetrics
description: Restituisce gli elementi di struttura (in DIP) del layout e tutti gli oggetti in esso contenuti, inclusi glifi di testo e oggetti inline.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Metodo GetOverhangMetrics Direct Write
- Metodo GetOverhangMetrics Direct Write, interfaccia IDWriteTextLayout
- Interfaccia IDWriteTextLayout Scrittura diretta, metodo GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3591df5dc02fdc63215ff2276202df62347ed21aef23991b4ddcadef094281
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649746"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>Metodo IDWriteTextLayout::GetOverhangMetrics

Restituisce gli elementi di struttura (in DIP) del layout e tutti gli oggetti in esso contenuti, inclusi glifi di testo e oggetti inline.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*overhangs* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWRITE \_ OVERHANG \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Overshoots of visible extents (in DIP) outside the layout( Overshoots of visible extents (in DIP) outside the layout( Overshoots of visible extents (in DIP) outside the layout.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le sottolineature e i barrati non contribuiscono alla determinazione black box, poiché vengono effettivamente disegnati dal renderer, che può disegnarli in qualsiasi varietà di stili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

