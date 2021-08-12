---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB funzione
description: Racchiude il valore XMFLOAT4 specificato in un UINT DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6661ea7bce5f5a10fec8c3d96bf178fc4e169ba53d013143b89c8114de71cc60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286837"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a>Da D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ FUNZIONE UNORM \_ SRGB

Racchiude il valore XMFLOAT4 specificato in un UINT DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB.

## <a name="syntax"></a>Sintassi

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Dati dello shader decompressi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dati dello shader di cui è stato effettuato il pacchetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni](format-conversion-functions.md)
</dt> <dt>

[Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





