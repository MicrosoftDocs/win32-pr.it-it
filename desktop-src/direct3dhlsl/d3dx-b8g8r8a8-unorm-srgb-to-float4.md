---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 funzione
description: Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB in XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 funzione
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620823a572b7eb23f05bdda83866aae982f326dfb70ca6856309abc9d96f05b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516597"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a>Funzione DA D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ a \_ FLOAT4

Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB in XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*packedInput* 
</dt> <dd>

Dati dello shader di cui è stato effettuato il pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati dello shader decompressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place delle immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





