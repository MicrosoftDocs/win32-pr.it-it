---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM funzione
description: Racchiude l'oggetto XMFLOAT4 specificato in un SNORM DXGI \_ FORMAT \_ R8G8B8A8. \_
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM funzione HLSL
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
ms.openlocfilehash: 0382cc5e7bfc47b8046eec437cbc25cf559c9116b4e6215cce9a3fb8f344f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286729"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a>Funzione SNORM da D3DX FLOAT4 a \_ \_ \_ R8G8B8A8 \_

Racchiude l'oggetto XMFLOAT4 specificato in un SNORM DXGI \_ FORMAT \_ R8G8B8A8. \_

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

Dati dello shader da creare come pacchetto.

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

 

 





