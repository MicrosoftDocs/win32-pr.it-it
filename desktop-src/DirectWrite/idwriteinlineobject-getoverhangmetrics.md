---
title: Metodo IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout chiama questa funzione di callback per ottenere gli extent visibili (in DIP) dell'oggetto inline. Nel caso di una bitmap semplice, senza riempimento e senza sporgenza, tutti i blocchi verranno semplicemente azzerati.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Scrittura diretta metodo GetOverhangMetrics
- Metodo GetOverhangMetrics scrittura diretta, interfaccia IDWriteInlineObject
- IDWriteInlineObject interface Direct Write, metodo GetOverhangMetrics
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
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330162"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>Metodo IDWriteInlineObject:: GetOverhangMetrics

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiama questa funzione di callback per ottenere gli extent visibili (in DIP) dell'oggetto inline. Nel caso di una bitmap semplice, senza riempimento e senza sporgenza, tutti i blocchi verranno semplicemente azzerati.

I blocchi devono essere restituiti rispetto alle dimensioni segnalate dell'oggetto (vedere le [**\_ \_ \_ metriche dell'oggetto inline DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) e non devono essere regolate dalla baseline.

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

Overshoot degli extent visibili (in DIP) all'esterno dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

