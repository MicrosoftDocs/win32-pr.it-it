---
title: Funzione D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
description: Comprime il XMFLOAT3 specificato in un formato DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- Funzione D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995855"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a>D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM \_ sRGB Function

Comprime il XMFLOAT3 specificato in un formato DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Dati dello shader da comprimere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati dello shader compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





