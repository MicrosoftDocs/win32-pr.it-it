---
description: Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Enumerazione D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355634"
---
# <a name="d3dx10_channel_flag-enumeration"></a>\_Enumerazione flag del canale d3dx10 \_

Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**\_Canale d3dx10 \_ rosso**
</dt> <dd>

Indica che deve essere utilizzato il canale rosso.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**\_Blu canale \_ d3dx10**
</dt> <dd>

Indica che deve essere utilizzato il canale blu.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Canale d3dx10 \_ verde**
</dt> <dd>

Indica che deve essere utilizzato il canale verde.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**\_Alfa canale \_ d3dx10**
</dt> <dd>

Indica che deve essere utilizzato il canale alfa.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_ \_ Luminanza canale d3dx10**
</dt> <dd>

Indica che deve essere utilizzato il luminaces dei canali rosso, verde e blu.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




