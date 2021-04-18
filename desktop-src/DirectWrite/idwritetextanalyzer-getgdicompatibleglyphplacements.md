---
title: Metodo IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements
description: Posizionare l'output dei glifi dal metodo GetGlyphs in base alle regole di rendering del tipo di carattere e del sistema di scrittura.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Scrittura diretta metodo GetGdiCompatibleGlyphPlacements
- Metodo GetGdiCompatibleGlyphPlacements scrittura diretta, interfaccia IDWriteTextAnalyzer
- IDWriteTextAnalyzer Interface Direct Write, metodo GetGdiCompatibleGlyphPlacements
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
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325292"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Metodo IDWriteTextAnalyzer:: GetGdiCompatibleGlyphPlacements

Posizionare l'output dei glifi dal metodo [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) in base alle regole di rendering del tipo di carattere e del sistema di scrittura.

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

*textString* \[ in\]
</dt> <dd>

Tipo: **const \* WCHAR**

Matrice di caratteri contenente la stringa originale da cui provengono i glifi.

</dd> <dt>

*ClusterMap* \[ in\]
</dt> <dd>

Tipo: **const \* UInt16**

Puntatore al mapping da intervalli di caratteri a intervalli di glifi. Questa operazione viene restituita da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textProps* \[ in\]
</dt> <dd>

Tipo: **[ **DWrite \_ shaping \_ \_ Proprietà testo**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Puntatore a una matrice di strutture che contiene le proprietà di shaping per ogni carattere. Questa struttura viene restituita da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UInt32**

Lunghezza del testo di *textString*.

</dd> <dt>

*GlyphIndices* \[ in\]
</dt> <dd>

Tipo: **const \* UInt16**

Matrice di indici di glifi restituiti da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphProps* \[ in\]
</dt> <dd>

Tipo: **const [**DWrite \_ shaping \_ Glyph \_ Properties**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

Puntatore a una matrice di strutture che contengono le proprietà di shaping per ogni glifo restituito da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UInt32**

Numero di glifi restituiti da [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*fontFace* \[ in\]
</dt> <dd>

Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Puntatore al tipo di carattere che rappresenta l'origine dei glifi di output.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Tipo: **float**

Dimensioni logiche del carattere in DIP.

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

 *isSideways* 
</dt> <dd>

Tipo: **bool**

Flag booleano impostato su **true** se il testo deve essere disegnato verticalmente.

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

Tipo: **bool**

Flag booleano impostato su **true** per il testo da destra a sinistra.

</dd> <dt>

 *scriptAnalysis* \[ in\]
</dt> <dd>

Tipo: **const [**DWrite \_ script \_ Analysis**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Puntatore a un risultato dell'analisi di script da una chiamata [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .

</dd> <dt>

 *localeName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* WCHAR**

Matrice di caratteri contenente le impostazioni locali da utilizzare per la selezione dei glifi. Ad esempio, lo stesso carattere può essere mappato a glifi diversi per ja-JP rispetto a ZH-CHS. Se è **null**, viene utilizzato il mapping predefinito basato sullo script.

</dd> <dt>

 *funzionalità* \[ di in, facoltativo\]
</dt> <dd>

Tipo: **\* \* const [**DWrite le \_ \_ funzionalità tipografiche**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**

Matrice di puntatori ai set di funzionalità tipografiche da utilizzare in ogni intervallo di funzionalità.

</dd> <dt>

 *featureRangeLengths* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const \* UInt32**

Lunghezza di ogni intervallo di funzioni, in caratteri. La somma di tutte le lunghezze deve essere uguale a *TextLength*.

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Tipo: **UInt32**

Numero di intervalli di funzioni.

</dd> <dt>

 *glyphAdvances* \[ out\]
</dt> <dd>

Tipo: **float \***

Quando termina, questo metodo contiene la larghezza di avanzamento di ogni glifo.

</dd> <dt>

 *GlyphOffsets* \[ out\]
</dt> <dd>

Tipo: **[ **\_ \_ offset glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Quando termina, questo metodo contiene l'offset dell'origine di ogni glifo.

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

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

