---
title: Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
description: Comprime il XMFLOAT4 specificato in un formato DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f61e484675b94e1089436ce0b3bd564b3103a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355769"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a>D3DX \_ float4 \_ to \_ R8G8B8A8 \_ UNORM \_ sRGB Function

Comprime il XMFLOAT4 specificato in un formato DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
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

 

 





