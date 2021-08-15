---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact funzione
description: Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB in XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact funzione
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact funzione HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b6fc32a06ff436046de76e212ef8f90a06338a55caa285865f12c98d6d4b068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793885"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>Funzione inesatta da D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ a \_ \_ FLOAT4

Decomprime i dati dello shader DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB in XMFLOAT4.

## <a name="syntax"></a>Sintassi

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

## <a name="remarks"></a>Commenti

Questa funzione usa istruzioni shader che non hanno una precisione sufficiente per fornire la risposta esatta. La funzione alternativa [**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB in \_ \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) usa una tabella di ricerca archiviata nello shader per fornire una conversione esatta da SRGB a float.

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

 

 





