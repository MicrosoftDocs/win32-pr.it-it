---
title: Funzione D3DX_R8G8B8A8_SINT_to_INT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 Sint shader in un XMINT4.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- Funzione D3DX_R8G8B8A8_SINT_to_INT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132362"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a>D3DX \_ R8G8B8A8 \_ \_ -funzione da Sint a \_ INT4

Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 Sint shader in un XMINT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
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

 

 





