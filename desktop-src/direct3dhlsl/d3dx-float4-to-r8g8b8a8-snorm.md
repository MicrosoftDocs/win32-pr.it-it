---
title: Funzione D3DX_FLOAT4_to_R8G8B8A8_SNORM
description: Comprime di nuovo il XMFLOAT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ russar.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- Funzione D3DX_FLOAT4_to_R8G8B8A8_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355779"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a>D3DX \_ float4 \_ to \_ R8G8B8A8 \_ russat Function

Comprime di nuovo il XMFLOAT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ russar.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
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

 

 





