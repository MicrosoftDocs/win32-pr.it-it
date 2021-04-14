---
title: Enumerazione D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Enumerazione D3DX11_CHANNEL_FLAG Direct3D 11
- Puntatore di enumerazione LPD3DX11_CHANNEL_FLAG Direct3D 11
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
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402026"
---
# <a name="d3dx11_channel_flag-enumeration"></a>\_Enumerazione flag del canale D3DX11 \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.

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

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**\_Canale D3DX11 \_ rosso**
</dt> <dd>

Indica che deve essere utilizzato il canale rosso.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**\_Blu canale \_ D3DX11**
</dt> <dd>

Indica che deve essere utilizzato il canale blu.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Canale D3DX11 \_ verde**
</dt> <dd>

Indica che deve essere utilizzato il canale verde.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**\_Alfa canale \_ D3DX11**
</dt> <dd>

Indica che deve essere utilizzato il canale alfa.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_ \_ Luminanza canale D3DX11**
</dt> <dd>

Indica che deve essere utilizzato il luminaces dei canali rosso, verde e blu.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





