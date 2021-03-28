---
title: Funzione D3DX_FLOAT2_to_R16G16_UNORM
description: Comprime il XMFLOAT2 specificato in un formato DXGI \_ \_ R16G16 \_ UNORM.
ms.assetid: 5a1bd034-262f-4f55-8f38-d2fda42bb13b
keywords:
- Funzione D3DX_FLOAT2_to_R16G16_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0a6ffe3081955db79765d80278394eb89ab188
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995906"
---
# <a name="d3dx_float2_to_r16g16_unorm-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ UNORM Function

Comprime il XMFLOAT2 specificato in un formato DXGI \_ \_ R16G16 \_ UNORM.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT2_to_R16G16_UNORM(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Dati dello shader decompressi.

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

 

 





