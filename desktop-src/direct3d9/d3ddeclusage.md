---
description: Identifica l'uso previsto dei dati dei vertici.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumerazione D3DDECLUSAGE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857511"
---
# <a name="d3ddeclusage-enumeration"></a>Enumerazione D3DDECLUSAGE

Identifica l'uso previsto dei dati dei vertici.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**POSIZIONE D3DDECLUSAGE \_**
</dt> <dd>

Posizionare i dati compresi tra (-1,-1) e (1,1). Usare D3DDECLUSAGE POSITION con un indice di utilizzo 0 per specificare la posizione non trasformata per l'elaborazione dei vertici di funzione fissa e il \_ tessellatore n patch. Usare D3DDECLUSAGE POSITION con un indice di utilizzo 1 per specificare la posizione non trasformata nel vertex shader a funzione fissa per la \_ tween dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

Fusione dei dati relativi al peso. Usare D3DDECLUSAGE BLENDWEIGHT con un indice di utilizzo 0 per specificare i pesi di blend usati nella fusione dei vertici indicizzata e \_ non indicizzata.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

Fusione dei dati degli indici. Usare D3DDECLUSAGE BLENDINDICES con un indice di utilizzo 0 per specificare gli indici di matrice per l'interfaccia con tavolozza \_ indicizzata.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**NORMALE D3DDECLUSAGE \_**
</dt> <dd>

Dati normali dei vertici. Usare D3DDECLUSAGE NORMAL con un indice di utilizzo 0 per specificare le normali dei vertici per l'elaborazione dei vertici delle funzioni fisse e il \_ tessellatore n patch. Usare D3DDECLUSAGE NORMAL con un indice di utilizzo 1 per specificare le normali dei vertici per l'elaborazione dei vertici a funzione fissa per la \_ tween dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**
</dt> <dd>

Dati relativi alle dimensioni dei punti. Usare D3DDECLUSAGE PSIZE con un indice di utilizzo 0 per specificare l'attributo point-size usato dal motore di installazione del rasterizzatore per espandere un punto in un quad per la funzionalità \_ point-sprite.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**
</dt> <dd>

Dati delle coordinate della trama. Usare D3DDECLUSAGE TEXCOORD, n per specificare le coordinate di trama nell'elaborazione dei vertici a funzione fissa e nei pixel shader precedenti a \_ ps \_ 3 \_ 0. Possono essere usati per passare dati definiti dall'utente.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**TANGENTE D3DDECLUSAGE \_**
</dt> <dd>

Dati della tangente dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BINORMAL**
</dt> <dd>

Dati binormali dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

Singolo valore a virgola mobile positivo. Usare D3DDECLUSAGE TESSFACTOR con un indice di utilizzo 0 per specificare un fattore a tessellazione usato nell'unità a tessellazione per controllare la frequenza di \_ sfasamento. Per altre informazioni sul tipo di dati, vedere D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ POSITIONT**
</dt> <dd>

I dati del vertice contengono dati di posizione trasformati compresi tra (0,0) e (larghezza del viewport, altezza del viewport). Usare D3DDECLUSAGE \_ POSITIONT con un indice di utilizzo 0 per specificare la posizione trasformata. Quando viene impostata una dichiarazione contenente questo oggetto, la pipeline non esegue l'elaborazione dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**COLORE D3DDECLUSAGE \_**
</dt> <dd>

I dati dei vertici contengono colori diffusi o speculari. Usare D3DDECLUSAGE COLOR con un indice di utilizzo 0 per specificare il colore diffuso nel vertex shader a funzione fissa e nei pixel shader precedenti \_ a ps \_ 3 \_ 0. Usare D3DDECLUSAGE COLOR con un indice di utilizzo di 1 per specificare il colore speculare nel vertex shader a funzione fissa e nei pixel shader precedenti \_ a ps \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ PIÙ**
</dt> <dd>

I dati dei vertici contengono i dati dei vertici. Usare D3DDECLUSAGEBIE con un indice di utilizzo pari a 0 per specificare un valore di sfumatura usato al termine dell'ombreggiatura \_ dei pixel. Questo vale per i pixel shader precedenti alla versione ps \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**PROFONDITÀ D3DDECLUSAGE \_**
</dt> <dd>

I dati dei vertici contengono dati di profondità.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**ESEMPIO D3DDECLUSAGE \_**
</dt> <dd>

I dati dei vertici contengono dati del campionatore. Usare D3DDECLUSAGE SAMPLE con un indice di utilizzo pari a 0 per specificare \_ il valore di spostamento da cercare. Può essere usato solo con D3DDECLUSAGE \_ LOOKUPPRESAMPLED o D3DDECLUSAGE \_ LOOKUP.

</dd> </dl>

## <a name="remarks"></a>Commenti

I dati dei vertici vengono dichiarati con una matrice [**di strutture D3DVERTEXELEMENT9.**](d3dvertexelement9.md) Ogni elemento nella matrice contiene un tipo di utilizzo.

Per altre informazioni sulle dichiarazioni dei vertici, vedere Dichiarazione dei vertici [(Direct3D 9).](vertex-declaration.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Dichiarazione vertice (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




