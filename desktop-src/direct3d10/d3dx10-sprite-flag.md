---
description: Flag sprite che specificano il comportamento dell'API di disegno dello sprite. Questi vengono passati in ID3DX10Sprite::Begin.
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: D3DX10_SPRITE_FLAG enumerazione (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 53b2c7965beaeb2976e88d38f5af90d546f644b6d4879964c23b2166cd51b19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634941"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>Enumerazione D3DX10 \_ SPRITE \_ FLAG

Flag sprite che specificano il comportamento dell'API di disegno dello sprite. Questi vengono passati in [**ID3DX10Sprite::Begin.**](id3dx10sprite-begin.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**TRAMA DI ORDINAMENTO \_ SPRITE D3DX10 \_ \_**
</dt> <dd>

Ordinare gli sprite in base alla trama prima del rendering in modo che quando sono presenti molti sprite con la stessa trama di cui verrà eseguito il rendering di tutti gli sprite contemporaneamente, migliorando così le prestazioni.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 \_ SPRITE \_ SORT \_ DEPTH \_ BACK \_ TO \_ FRONT**
</dt> <dd>

Ordinare gli sprite da dietro all'inizio per fare in modo che quelli più distorsi dalla fotocamera verranno disegnati per primi.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ SPRITE \_ SORT \_ DEPTH \_ FRONT \_ TO \_ BACK**
</dt> <dd>

Ordinare gli sprite dall'inizio alla posteriore in modo che quelli più vicini alla fotocamera siano disegnati per primi.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ SPRITE \_ SAVE \_ STATE**
</dt> <dd>

Salva lo stato in modo che, quando viene chiamato [**ID3DX10Sprite::End,**](id3dx10sprite-end.md) lo stato venga ripristinato nel modo precedente a [**ID3DX10Sprite::Begin.**](id3dx10sprite-begin.md)

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**TRAME D3DX10 \_ SPRITE \_ ADDREF \_**
</dt> <dd>

Chiama AddRef su tutte le trame quando vengono passate in [**ID3DX10Sprite::D rawSpritesBuffered.**](id3dx10sprite-drawspritesbuffered.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Al termine di un ordinamento front-to-back o back-to-front, verrà eseguito automaticamente un ordinamento secondario per trama. Ciò è utile quando sono presenti molti sprite con la stessa trama tutti sullo stesso piano, ad esempio quando si disegna l'interfaccia utente in un gioco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




