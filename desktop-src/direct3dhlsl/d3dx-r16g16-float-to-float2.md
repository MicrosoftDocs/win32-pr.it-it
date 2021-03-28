---
title: Funzione D3DX_R16G16_FLOAT_to_FLOAT2
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- Funzione D3DX_R16G16_FLOAT_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132394"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a>D3DX \_ R16G16 \_ float \_ to \_ FLOAT2 Function

Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT2.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
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

 

 





