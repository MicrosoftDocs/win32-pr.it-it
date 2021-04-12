---
title: Metodo IDWriteFactory2 CreateCustomRenderingParams
description: Crea un oggetto parametri di rendering con le proprietà specificate.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Scrittura diretta metodo CreateCustomRenderingParams
- Metodo CreateCustomRenderingParams scrittura diretta, interfaccia IDWriteFactory2
- IDWriteFactory2 Interface Direct Write, metodo CreateCustomRenderingParams
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400759"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>Metodo IDWriteFactory2:: CreateCustomRenderingParams

Crea un oggetto parametri di rendering con le proprietà specificate.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*gamma* 
</dt> <dd>

Tipo: **float**

Valore gamma usato per la correzione gamma, che deve essere maggiore di zero e non può essere superiore a 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Tipo: **float**

Quantità di miglioramento del contrasto, zero o superiore.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Tipo: **float**

Quantità di miglioramento del contrasto, zero o superiore.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Tipo: **float**

Grado di livello ClearType, da 0,0 f (senza ClearType) a 1,0 f (ClearType completo).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Tipo: **[ **DWrite \_ pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Geometria di un pixel del dispositivo.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **[ **\_ \_ modalità di rendering DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Metodo di rendering dei glifi. Nella maggior parte dei casi, è consigliabile \_ \_ usare la modalità di rendering DWrite \_ per impostazione predefinita per usare automaticamente una modalità appropriata.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWrite \_ Grid \_ Fit \_ mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Come grigliare i delineamenti dell'icona adatta. Nella maggior parte dei casi, deve essere DWRITE \_ Grid \_ Fit \_ default per scegliere automaticamente una modalità appropriata.

</dd> <dt>

*renderingParams* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Include l'oggetto parametri di rendering appena creato oppure NULL in caso di errore.

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

 

