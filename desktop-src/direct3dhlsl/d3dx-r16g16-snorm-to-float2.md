---
title: D3DX_R16G16_SNORM_to_FLOAT2 funzione
description: Decomprime i dati dello \_ shader DXGI FORMAT \_ R16G16 \_ SNORM in XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- D3DX_R16G16_SNORM_to_FLOAT2 funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589954208886b7dccf4f48d2724c98ab4404d5394b73d894a8eb4924e152cdcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983241"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a>Da D3DX \_ R16G16 \_ SNORM \_ a funzione \_ FLOAT2

Decomprime i dati dello \_ shader DXGI FORMAT \_ R16G16 \_ SNORM in XMFLOAT2.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
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

 

 





