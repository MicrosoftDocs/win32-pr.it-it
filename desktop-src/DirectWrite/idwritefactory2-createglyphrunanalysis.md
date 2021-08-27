---
title: Metodo IDWriteFactory2 CreateGlyphRunAnalysis
description: Crea un oggetto di analisi dell'esecuzione del glifo, che incapsula le informazioni usate per eseguire il rendering di un'esecuzione di glifi.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Metodo CreateGlyphRunAnalysis Direct Write
- Metodo CreateGlyphRunAnalysis Direct Write, interfaccia IDWriteFactory2
- Interfaccia IDWriteFactory2 Direct Write, metodo CreateGlyphRunAnalysis
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
ms.openlocfilehash: c4ea5c2dc4cb97b1b9ba02e786efc20a4e2a44990b9a1d28b862aeab254079a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048831"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>Metodo IDWriteFactory2::CreateGlyphRunAnalysis

Crea un oggetto di analisi dell'esecuzione del glifo, che incapsula le informazioni usate per eseguire il rendering di un'esecuzione di glifi.

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

*glyphRun* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

Struttura che specifica le proprietà dell'esecuzione del glifo.

</dd> <dt>

*trasformazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Trasformazione facoltativa applicata ai glifi e alle relative posizioni. Questa trasformazione viene applicata dopo il ridimensionamento specificato da emSize e pixelsPerDip.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **MODALITÀ DI RENDERING \_ \_ DWRITE**

Specifica la modalità di rendering, che deve essere una delle modalità di rendering raster, ovvero non predefinita e non di struttura.

</dd> <dt>

*modalità di misurazione* 
</dt> <dd>

Tipo: **[ **MODALITÀ DI \_ MISURAZIONE \_ DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Specifica il metodo per misurare i glifi.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ GRID \_ FIT \_ MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Come adattare alla griglia i contorni dei glifi. Deve essere non predefinito.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Tipo: **[ **MODALITÀ \_ \_ ANTIALIAS DWRITE \_ TEXT**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Specifica la modalità antialias.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Tipo: **FLOAT**

Posizione orizzontale dell'origine della linea di base, in DIP.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Tipo: **FLOAT**

Posizione verticale dell'origine della baseline, in DIP.

</dd> <dt>

*glifoRunAnalysis* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Riceve un puntatore all'oggetto appena creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

