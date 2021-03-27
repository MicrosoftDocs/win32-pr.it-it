---
title: Funzione D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM \_ sRGB shader in un XMFLOAT4. | Funzione D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- Funzione D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e373ccb8035b19da7c44ee05a07dd0351ca8f48d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982175"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ float4 Function

Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM \_ sRGB shader in un XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*packedInput* 
</dt> <dd>

Dati dello shader compressi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati dello shader decompressi.

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

 

 





