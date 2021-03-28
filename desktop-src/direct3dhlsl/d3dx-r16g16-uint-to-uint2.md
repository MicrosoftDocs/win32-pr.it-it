---
title: Funzione D3DX_R16G16_UINT_to_UINT2
description: Decomprime \_ \_ \_ i dati di DXGI Format R16G16 uint shader in un XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- Funzione D3DX_R16G16_UINT_to_UINT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2586ff8876ee10368d49b816b38f5c9c8caf7c7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354044"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a>D3DX \_ R16G16 \_ uint \_ to \_ UINT2 Function

Decomprime \_ \_ \_ i dati di DXGI Format R16G16 uint shader in un XMUINT2.

## <a name="syntax"></a>Sintassi

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
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

 

 





