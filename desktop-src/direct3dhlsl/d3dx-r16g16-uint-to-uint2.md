---
title: D3DX_R16G16_UINT_to_UINT2 funzione
description: Decomprime i dati dello shader UINT DXGI \_ FORMAT \_ R16G16 \_ in XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- D3DX_R16G16_UINT_to_UINT2 funzione HLSL
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
ms.openlocfilehash: 15e2d31194364c865d8f6ae77a838e8f64f2c153b4185a8f3d26e32737835dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726911"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a>Da D3DX \_ R16G16 \_ UINT \_ alla funzione \_ UINT2

Decomprime i dati dello shader UINT DXGI \_ FORMAT \_ R16G16 \_ in XMUINT2.

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

[Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





