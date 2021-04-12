---
title: Metodo IDWriteFactory2 CreateGlyphRunAnalysis
description: Crea un oggetto di analisi dell'esecuzione del glifo che incapsula le informazioni utilizzate per il rendering di un'esecuzione del glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Scrittura diretta metodo CreateGlyphRunAnalysis
- Metodo CreateGlyphRunAnalysis scrittura diretta, interfaccia IDWriteFactory2
- IDWriteFactory2 Interface Direct Write, metodo CreateGlyphRunAnalysis
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400758"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>Metodo IDWriteFactory2:: CreateGlyphRunAnalysis

Crea un oggetto di analisi dell'esecuzione del glifo che incapsula le informazioni utilizzate per il rendering di un'esecuzione del glifo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*GlyphRun* \[ in\]
</dt> <dd>

Tipo: **const [**DWrite \_ glifo \_ Run**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _

Struttura che specifica le proprietà dell'esecuzione del glifo.

</dd> <dt>

_transform * \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWrite \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _

Trasformazione facoltativa applicata ai glifi e alle rispettive posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato da emSize e pixelsPerDip.

</dd> <dt>

_renderingMode * 
</dt> <dd>

Tipo: **\_ \_ modalità di rendering DWrite**

Specifica la modalità di rendering, che deve essere una delle modalità di rendering raster (ovvero non predefinita e non struttura).

</dd> <dt>

*measuringMode* 
</dt> <dd>

Tipo: **[ **\_ \_ modalità di misurazione DWrite**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Specifica il metodo per misurare i glifi.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWrite \_ Grid \_ Fit \_ mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Come grigliare le strutture di glifi. Deve essere non predefinito.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Tipo: **[ **DWrite \_ Text \_ antialias \_ mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Specifica la modalità antialias.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Tipo: **float**

Posizione orizzontale dell'origine della linea di base, in DIP.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Tipo: **float**

Posizione verticale dell'origine della linea di base, in DIP.

</dd> <dt>

*glyphRunAnalysis* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Riceve un puntatore all'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

