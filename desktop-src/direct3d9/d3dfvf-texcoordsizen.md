---
description: Costruisce modelli di bit utilizzati per identificare i formati delle coordinate di trama all'interno di una descrizione FVF. I risultati di queste macro possono essere combinati all'interno di una descrizione FVF usando l'operatore OR.
ms.assetid: c3076d7c-7935-40ee-b513-7ff6551a535f
title: D3DFVF_TEXCOORDSIZEN (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFVF_TEXCOORDSIZEN
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 58288667954e3414aa3d8ae1550e02e7216ffb4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322937"
---
# <a name="d3dfvf_texcoordsizen"></a>\_TEXCOORDSIZEN D3DFVF

Costruisce modelli di bit utilizzati per identificare i formati delle coordinate di trama all'interno di una descrizione FVF. I risultati di queste macro possono essere combinati all'interno di una descrizione FVF usando l'operatore OR.

``` syntax
#define D3DFVF_TEXCOORDSIZEN(CoordIndex) 
#define D3DFVF_TEXCOORDSIZE1(CoordIndex) (D3DFVF_TEXTUREFORMAT1 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE2(CoordIndex) (D3DFVF_TEXTUREFORMAT2) 
#define D3DFVF_TEXCOORDSIZE3(CoordIndex) (D3DFVF_TEXTUREFORMAT3 << (CoordIndex*2 + 16)) 
#define D3DFVF_TEXCOORDSIZE4(CoordIndex) (D3DFVF_TEXTUREFORMAT4 << (CoordIndex*2 + 16))
```

## <a name="parameters"></a>Parametri



| Parametro                                                                                                    | Descrizione                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CoordIndex"></span><span id="coordindex"></span><span id="COORDINDEX"></span>CoordIndex<br/> | Valore che identifica il set di coordinate di trama a cui si applicano le dimensioni della coordinata di trama (1-, 2-, 3-o 4Dimensional). <br/> |



 

## <a name="remarks"></a>Commenti

Le **macro \_ TEXCOORDSIZEN D3DFVF** utilizzano le costanti seguenti.


```C++
#define D3DFVF_TEXTUREFORMAT1 3 // one floating point value
#define D3DFVF_TEXTUREFORMAT2 0 // two floating point values
#define D3DFVF_TEXTUREFORMAT3 1 // three floating point values
#define D3DFVF_TEXTUREFORMAT4 2 // four floating point values
```



La descrizione di FVF seguente identifica un formato di vertice con una posizione; normale; colori diffusi e speculari; e due set di coordinate di trama. Il primo set di coordinate di trama include un singolo elemento e il secondo set include due elementi:


```C++
DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE |
              D3DFVF_SPECULAR | D3DFVF_TEX2 |
              D3DFVF_TEXCOORDSIZE1(0) |  // Uses 1D texture coordinates for
                                         // texture coordinate set 1 (index 0).
              D3DFVF_TEXCOORDSIZE2(1);   // And 2D texture coordinates for 
                                         // texture coordinate set 2 (index 1).
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DFVF](d3dfvf.md)
</dt> </dl>

 

 




