---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- ByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb7a22570e92945df8ab599f8c95bdffa1d03dd9ac83e35dfc7bb849bd42d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853331"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Buffer di sola lettura indicizzato in byte.



| Metodo                                                              | Descrizione                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](byteaddressbuffer-load.md)                              | Ottiene un valore.               |
| [**Carica2**](byteaddressbuffer-load2.md)                            | Ottiene due valori.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Ottiene tre valori.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Ottiene quattro valori.             |



 

È possibile usare il **tipo di oggetto ByteAddressBuffer** quando si usano buffer non elaborati. Per altre informazioni sulla visualizzazione non elaborata dei buffer, vedere [Viste non elaborate dei buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Supportato |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Modelli shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive [Shader Model 4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10.0 o 10.1 ([**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 X) nei dispositivi che supportano gli shader di \_ calcolo. Per altre informazioni sul supporto dello shader di calcolo nell'hardware di livello inferiore, vedere [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)(Shader di calcolo su hardware di livello inferiore).<br/> | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Per altre informazioni su un buffer di indirizzi di byte, vedere il tipo [di risorsa indirizzabile ai byte](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

Shader Model 5 implementa anche un [buffer di indirizzi di byte di lettura/scrittura.](sm5-object-rwbyteaddressbuffer.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti modello shader 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

