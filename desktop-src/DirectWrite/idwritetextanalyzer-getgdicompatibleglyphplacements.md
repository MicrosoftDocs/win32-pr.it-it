---
title: Metodo IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements
description: Inserire l'output dei glifi dal metodo GetGlyphs in base al tipo di carattere e alle regole di rendering del sistema di scrittura.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Metodo GetGdiCompatibleGlyphPlacements Direct Write
- Metodo GetGdiCompatibleGlyphPlacements Direct Write, interfaccia IDWriteTextAnalyzer
- Metodo GetGdiCompatibleGlyphPlacements dell'interfaccia IDWriteTextAnalyzer
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d05fcf5595500f34730a720e4a4c2e80d68922929d8055b754a26a1dc92f63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650011"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Metodo IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements

Inserire l'output dei glifi dal [**metodo GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) in base al tipo di carattere e alle regole di rendering del sistema di scrittura.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*textString* \[ Pollici\]
</dt> <dd>

Tipo: **const \* WCHAR**

Matrice di caratteri contenente la stringa originale da cui provenivano i glifi.

</dd> <dt>

*clusterMap* \[ Pollici\]
</dt> <dd>

Tipo: **const UINT16 \***

Puntatore al mapping dagli intervalli di caratteri agli intervalli di glifi. Viene restituito da [**GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*textProps* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWRITE \_ SHAPING \_ TEXT \_ PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Puntatore a una matrice di strutture che contiene le proprietà di data shaping per ogni carattere. Questa struttura viene restituita [**da GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

Lunghezza del testo di *textString.*

</dd> <dt>

*glifoIndices* \[ Pollici\]
</dt> <dd>

Tipo: **const UINT16 \***

Matrice di indici di glifi restituiti da [**GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*glyphProps* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWRITE \_ SHAPING \_ GLYPH \_ PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

Puntatore a una matrice di strutture che contengono proprietà di data shaping per ogni glifo restituito da [**GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

Numero di glifi restituiti da [**GetGlyphs.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)

</dd> <dt>

*carattere Carattere* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Puntatore al tipo di carattere che rappresenta l'origine per i glifi di output.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Tipo: **FLOAT**

Dimensione logica del carattere in DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **FLOAT**

Numero di pixel fisici per DIP.

</dd> <dt>

*trasformazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Trasformazione facoltativa applicata ai glifi e alle relative posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato dalle dimensioni del carattere e *pixelPerDip.*

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **BOOL**

Se impostata **su FALSE,** le metriche sono le stesse del testo con alias GDI. Se impostata **su TRUE,** le metriche sono le stesse del testo misurato da GDI usando un tipo di carattere creato con **CLEARTYPE \_ NATURAL \_ QUALITY.**

</dd> <dt>

 *isSideways* 
</dt> <dd>

Tipo: **BOOL**

Flag booleano impostato su **TRUE se** il testo deve essere disegnato verticalmente.

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

Tipo: **BOOL**

Flag booleano impostato su **TRUE per** il testo da destra a sinistra.

</dd> <dt>

 *scriptAnalysis* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWRITE \_ SCRIPT \_ ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Puntatore a un risultato dell'analisi dello script da [**una chiamata AnalyzeScript.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript)

</dd> <dt>

 *localeName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* WCHAR**

Matrice di caratteri contenente le impostazioni locali da utilizzare per la selezione dei glifi. Ad esempio, lo stesso carattere può essere mappato a glifi diversi per ja-jp e zh-chs. Se è **NULL,** viene usato il mapping predefinito basato sullo script.

</dd> <dt>

 *funzionalità* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWRITE \_ \_ TYPOGRAPHIC FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

Matrice di puntatori ai set di caratteristiche tipografiche da usare in ogni intervallo di caratteristiche.

</dd> <dt>

 *featureRangeLengths* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const UINT32 \***

Lunghezza di ogni intervallo di caratteristiche, in caratteri. La somma di tutte le lunghezze deve essere uguale a *textLength.*

</dd> <dt>

 *Oggetti featureRanges* 
</dt> <dd>

Tipo: **UINT32**

Numero di intervalli di funzionalità.

</dd> <dt>

 *glyphAdvances* \[ Cambio\]
</dt> <dd>

Tipo: **\* FLOAT**

Quando questo metodo viene restituito, contiene la larghezza di avanzamento di ogni glifo.

</dd> <dt>

 *glyphOffsets* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWRITE \_ GLYPH \_ OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Quando questo metodo viene restituito, contiene l'offset dell'origine di ogni glifo.

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

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

