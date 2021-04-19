---
title: Metodo IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Ottiene le metriche del glifo in unità di progettazione dei tipi di carattere con i valori restituiti compatibili con i prodotti GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Scrittura diretta metodo GetGdiCompatibleGlyphMetrics
- Metodo GetGdiCompatibleGlyphMetrics scrittura diretta, interfaccia IDWriteFontFace
- IDWriteFontFace interface Direct Write, metodo GetGdiCompatibleGlyphMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330034"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Metodo IDWriteFontFace:: GetGdiCompatibleGlyphMetrics

Ottiene le metriche del glifo in unità di progettazione dei tipi di carattere con i valori restituiti compatibili con i prodotti GDI.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*emSize* 
</dt> <dd>

Tipo: **float**

Dimensioni ogico del tipo di carattere in unità DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **float**

Il numero di pixel fisici per DIP.

</dd> <dt>

*trasformazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e da *pixelsPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **bool**

Se è impostato su **false**, le metriche corrispondono a quelle del testo con aliasing GDI. Quando è impostato su **true**, le metriche corrispondono a quelle del testo misurato da GDI usando un tipo di carattere creato con la **\_ \_ qualità naturale CLEARTYPE**.

</dd> <dt>

*GlyphIndices* \[ in\]
</dt> <dd>

Tipo: **const \* UInt16**

Matrice di indici di glifi per i quali calcolare la metrica.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UInt32**

Numero di elementi nella matrice *GlyphIndices* .

</dd> <dt>

*glyphMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **\_ \_ metrica glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Matrice di strutture [**della \_ \_ metrica del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) riempite da questa funzione. Le metriche si trovano in unità di progettazione dei tipi di carattere.

</dd> <dt>

*isSideways* 
</dt> <dd>

Tipo: **bool**

Valore BOOL che indica se il tipo di carattere viene utilizzato in un'esecuzione laterale. Questo può influire sulle metriche del glifo se il tipo di carattere presenta una simulazione obliqua perché la simulazione obliqua laterale differisce dalla simulazione obliqua non laterale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Codice di errore **HRESULT** standard. Se uno degli indici del glifo di input è esterno all'intervallo di indice del glifo valido per il tipo di carattere corrente, verrà restituito **E \_ INVALIDARG** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

