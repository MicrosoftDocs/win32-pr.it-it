---
title: Metodo IDWriteFactory2 CreateCustomRenderingParams
description: Crea un oggetto parametri di rendering con le proprietà specificate.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Metodo CreateCustomRenderingParams Direct Write
- Metodo CreateCustomRenderingParams Direct Write, interfaccia IDWriteFactory2
- Metodo CreateCustomRenderingParams dell'interfaccia IDWriteFactory2 Direct Write
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
ms.openlocfilehash: 2e85057c28e1ad969fe72711c86aab9657126c760ea3041a08bc5101877686a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071692"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>Metodo IDWriteFactory2::CreateCustomRenderingParams

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

Tipo: **FLOAT**

Valore gamma utilizzato per la correzione gamma, che deve essere maggiore di zero e non può superare 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Tipo: **FLOAT**

Quantità di miglioramento del contrasto, zero o superiore.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Tipo: **FLOAT**

Quantità di miglioramento del contrasto, zero o superiore.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Tipo: **FLOAT**

Grado di livello ClearType, da 0,0f (nessun ClearType) a 1,0f (ClearType completo).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Tipo: **[ **DWRITE \_ PIXEL \_ GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Geometria di un pixel del dispositivo.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **[ **MODALITÀ DI \_ RENDERING \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Metodo di rendering dei glifi. Nella maggior parte dei casi, deve essere DWRITE \_ RENDERING MODE DEFAULT per usare \_ \_ automaticamente una modalità appropriata.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ GRID \_ FIT \_ MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Come adattare alla griglia i contorni dei glifi. Nella maggior parte dei casi, deve essere DWRITE \_ GRID FIT DEFAULT per scegliere \_ \_ automaticamente una modalità appropriata.

</dd> <dt>

*renderingParams* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Contiene l'oggetto parametri di rendering appena creato o NULL in caso di errore.

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

 

