---
title: D3DX11_CHANNEL_FLAG enumerazione (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Questi flag vengono usati dalle funzioni che operano su uno o più canali in una trama.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG enumerazione Direct3D 11
- LPD3DX11_CHANNEL_FLAG puntatore di enumerazione Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f8142d34235a151638e1043928521666f2d1751319ee785d22b92004a14421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028311"
---
# <a name="d3dx11_channel_flag-enumeration"></a>Enumerazione CHANNEL FLAG D3DX11 \_ \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.

 

Questi flag vengono usati dalle funzioni che operano su uno o più canali in una trama.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 \_ CHANNEL \_ RED**
</dt> <dd>

Indica che deve essere usato il canale rosso.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 \_ CHANNEL \_ BLUE**
</dt> <dd>

Indica che deve essere utilizzato il canale blu.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**VERDE CANALE D3DX11 \_ \_**
</dt> <dd>

Indica che deve essere usato il canale verde.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11 \_ CHANNEL \_ ALPHA**
</dt> <dd>

Indica che deve essere usato il canale alfa.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**LUMINANCE DEL CANALE D3DX11 \_ \_**
</dt> <dd>

Indica che devono essere usate le luminesi dei canali rosso, verde e blu.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





