---
title: Funzione D3DX_FLOAT2_to_R16G16_SNORM
description: Comprime di nuovo il XMFLOAT2 specificato in un \_ formato DXGI \_ R16G16 \_ russar.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- Funzione D3DX_FLOAT2_to_R16G16_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969388"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ russat Function

Comprime di nuovo il XMFLOAT2 specificato in un \_ formato DXGI \_ R16G16 \_ russar.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
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

 

 





