---
description: "Flag sprite che indicano all'API di disegno sprite come si comportano. Questi vengono passati in ID3DX10Sprite:: Begin."
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Enumerazione D3DX10_SPRITE_FLAG (D3DX10Core. h)
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
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323383"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>\_ \_ Enumerazione flag d3dx10 sprite

Flag sprite che indicano all'API di disegno sprite come si comportano. Questi vengono passati in [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).

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

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Trama di \_ ordinamento \_ sprite d3dx10**
</dt> <dd>

Ordinare gli sprite in base alla trama prima del rendering in modo che, quando ci sono molti sprite con la stessa trama che verrà eseguito il rendering di tutti gli sprite, in modo da migliorare le prestazioni.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**\_ \_ \_ Profondità di ordinamento sprite \_ di d3dx10 \_ di nuovo in \_ primo piano**
</dt> <dd>

Ordinare gli sprite da un inizio all'altra per fare in modo che quelli più lontani dalla fotocamera vengano disegnati per primi.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**\_ \_ Profondità di ordinamento dello sprite d3dx10 \_ \_ \_ da fronte a \_ sfondo**
</dt> <dd>

Ordinare gli sprite dalla parte anteriore a quella posteriore in modo da disegnare prima quelli più vicini alla fotocamera.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**\_ \_ Stato salvataggio sprite \_ d3dx10**
</dt> <dd>

Salva lo stato in modo che quando viene chiamato [**ID3DX10Sprite:: end**](id3dx10sprite-end.md) , lo stato viene ripristinato come prima della chiamata a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) .

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**\_ \_ Trame d3dx10 sprite ADDREF \_**
</dt> <dd>

Chiama AddRef su tutte le trame quando vengono passate in [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Dopo l'esecuzione di un ordinamento front-to-back o back-to-front, viene eseguito automaticamente un ordinamento secondario per trama. Questa operazione è utile quando sono presenti molti sprite con la stessa trama nello stesso piano, ad esempio quando si disegna l'interfaccia utente in un gioco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




