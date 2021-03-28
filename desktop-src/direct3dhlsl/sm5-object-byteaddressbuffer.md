---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- HLSL ByteAddressBuffer
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976826"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Buffer di sola lettura indicizzato in byte.



| Metodo                                                              | Descrizione                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Ottiene le dimensioni della risorsa. |
| [**Caricamento**](byteaddressbuffer-load.md)                              | Ottiene un valore.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Ottiene due valori.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Ottiene tre valori.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Ottiene quattro valori.             |



 

È possibile utilizzare il tipo di oggetto **ByteAddressBuffer** quando si utilizzano buffer non elaborati. Per altre informazioni sulla visualizzazione non elaborata dei buffer, vedere [visualizzazioni non elaborate dei buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Supportato |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10,0 o 10,1 ([**D3D \_ feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sui dispositivi che supportano compute shader. Per altre informazioni sul supporto di compute shader nell'hardware di livello inferiore, vedere [Compute Shaders su hardware di livello inferiore](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).<br/> | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Per ulteriori informazioni su un buffer degli indirizzi byte, vedere il [tipo di risorsa indirizzabile di byte](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

Shader Model 5 implementa anche un [buffer di indirizzi byte di lettura e scrittura](sm5-object-rwbyteaddressbuffer.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

