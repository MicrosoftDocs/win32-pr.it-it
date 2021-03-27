---
title: Funzione D3DX_R16G16_SINT_to_INT2
description: Decomprime \_ \_ \_ i dati di DXGI Format R16G16 Sint shader in un XMINT2.
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- Funzione D3DX_R16G16_SINT_to_INT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996153"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a>D3DX \_ R16G16 \_ \_ -funzione da Sint a \_ int2

Decomprime \_ \_ \_ i dati di DXGI Format R16G16 Sint shader in un XMINT2.

## <a name="syntax"></a>Sintassi

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
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

 

 





