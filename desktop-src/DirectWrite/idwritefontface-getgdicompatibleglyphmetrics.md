---
title: Metodo IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Ottiene le metriche dei glifi nelle unità di progettazione dei tipi di carattere con i valori restituiti compatibili con il prodotto GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Metodo GetGdiCompatibleGlyphMetrics Direct Write
- Metodo GetGdiCompatibleGlyphMetrics Direct Write, interfaccia IDWriteFontFace
- Interfaccia IDWriteFontFace Direct Write, metodo GetGdiCompatibleGlyphMetrics
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
ms.openlocfilehash: bd36fc09ff8161ba8fb72d3b55b9351b0a7d2a6bd3f3f11a71c15a8d9422f6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816501"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Metodo IDWriteFontFace::GetGdiCompatibleGlyphMetrics

Ottiene le metriche dei glifi nelle unità di progettazione dei tipi di carattere con i valori restituiti compatibili con il prodotto GDI.

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

Tipo: **FLOAT**

Dimensione ogica del tipo di carattere in unità DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **FLOAT**

Numero di pixel fisici per DIP.

</dd> <dt>

*trasformazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Trasformazione facoltativa applicata ai glifi e alle relative posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e *pixelPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **BOOL**

Se impostato su **FALSE,** le metriche sono le stesse delle metriche del testo con alias GDI. Se impostato su **TRUE,** le metriche sono le stesse del testo misurato da GDI usando un tipo di carattere creato con **CLEARTYPE \_ NATURAL \_ QUALITY.**

</dd> <dt>

*glifoIndices* \[ Pollici\]
</dt> <dd>

Tipo: **const UINT16 \***

Matrice di indici di glifi per cui calcolare le metriche.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

Numero di elementi nella matrice *glyphIndices.*

</dd> <dt>

*glyphMetrics* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWRITE \_ GLYPH \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Matrice di [**strutture DWRITE \_ GLYPH \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) riempite da questa funzione. Le metriche sono in unità di progettazione dei tipi di carattere.

</dd> <dt>

*isSideways* 
</dt> <dd>

Tipo: **BOOL**

Valore BOOL che indica se il tipo di carattere viene usato in un'esecuzione laterale. Ciò può influire sulle metriche degli glifi se il tipo di carattere ha una simulazione obliqua perché la simulazione obliqua laterale differisce dalla simulazione obliqua non laterale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Codice **di errore HRESULT** standard. Se uno degli indici del glifo di input non è compreso nell'intervallo di indici del glifo valido per il carattere corrente, verrà restituito **E \_ INVALIDARG.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

