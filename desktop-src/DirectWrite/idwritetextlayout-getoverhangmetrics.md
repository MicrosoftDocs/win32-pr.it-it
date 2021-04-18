---
title: Metodo IDWriteTextLayout GetOverhangMetrics
description: Restituisce i blocchi (in DIP) del layout e tutti gli oggetti in esso contenuti, inclusi i glifi di testo e gli oggetti inline.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Scrittura diretta metodo GetOverhangMetrics
- Metodo GetOverhangMetrics scrittura diretta, interfaccia IDWriteTextLayout
- IDWriteTextLayout Interface Direct Write, metodo GetOverhangMetrics
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
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328148"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>Metodo IDWriteTextLayout:: GetOverhangMetrics

Restituisce i blocchi (in DIP) del layout e tutti gli oggetti in esso contenuti, inclusi i glifi di testo e gli oggetti inline.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*blocchi* \[ out\]
</dt> <dd>

Tipo: **[ **\_ \_ metrica di sporgenza DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Overshoot degli extent visibili (in DIP) all'esterno del layout.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le sottolineature e strikethroughs non contribuiscono alla determinazione black box, perché vengono effettivamente disegnate dal renderer, che può essere disegnate in qualsiasi varietà di stili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

