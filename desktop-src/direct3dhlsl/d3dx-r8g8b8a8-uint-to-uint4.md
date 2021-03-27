---
title: Funzione D3DX_R8G8B8A8_UINT_to_UINT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 uint shader in un XMUINT4.
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- Funzione D3DX_R8G8B8A8_UINT_to_UINT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a371a36e797e1bff17aff457e11b140e4775894
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982211"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a>D3DX \_ R8G8B8A8 \_ uint \_ to \_ UINT4 Function

Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 uint shader in un XMUINT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
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

 

 





