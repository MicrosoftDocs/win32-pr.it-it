---
title: Funzione D3DX_UINT2_to_R16G16_UINT
description: Comprime di nuovo il XMUINT2 specificato in un \_ formato DXGI \_ R16G16 \_ uint.
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- Funzione D3DX_UINT2_to_R16G16_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59a20b62fc5d8078152ed483ae49afceeeda4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995885"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a>D3DX \_ UINT2 \_ a \_ R16G16 \_ uint Function

Comprime di nuovo il XMUINT2 specificato in un \_ formato DXGI \_ R16G16 \_ uint.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
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

 

 





