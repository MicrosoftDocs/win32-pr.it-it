---
title: Metodo IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout chiama questa funzione di callback per ottenere gli extent visibili (in DIP) dell'oggetto inline. Nel caso di una bitmap semplice, senza spaziatura interna e senza sporgenza, tutte le sporgenze saranno semplicemente zeri.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Metodo GetOverhangMetrics Direct Write
- Metodo GetOverhangMetrics Direct Write, interfaccia IDWriteInlineObject
- Interfaccia IDWriteInlineObject Direct Write, metodo GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 011794fc3804435dd565a00035247436814c41474c60b66f90c5cb5d9594f6c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928151"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>Metodo IDWriteInlineObject::GetOverhangMetrics

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiama questa funzione di callback per ottenere gli extent visibili (in DIP) dell'oggetto inline. Nel caso di una bitmap semplice, senza spaziatura interna e senza sporgenza, tutte le sporgenze saranno semplicemente zeri.

Le sporgenze devono essere restituite in relazione alle dimensioni segnalate dell'oggetto (vedere [**DWRITE \_ INLINE \_ OBJECT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) e non devono essere regolate in base alla linea di base.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sporgenze* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWRITE \_ OVERHANG \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Overshoot di extent visibili (in DIP) all'esterno dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

