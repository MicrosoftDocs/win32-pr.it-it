---
description: Identifica l'uso previsto dei dati dei vertici.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumerazione D3DDECLUSAGE (D3D9Types. h)
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
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322410"
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

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Posizione D3DDECLUSAGE**
</dt> <dd>

Posizionare i dati compresi tra (-1,-1) e (1, 1). Usare \_ la posizione D3DDECLUSAGE con un indice di utilizzo 0 per specificare la posizione non trasformata per l'elaborazione del vertice della funzione fissa e l'mosaico n-patch. Usare la \_ posizione D3DDECLUSAGE con un indice di utilizzo 1 per specificare una posizione non trasformata nel vertex shader della funzione fissa per l'interpolazione dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**\_BLENDWEIGHT D3DDECLUSAGE**
</dt> <dd>

Fusione dei dati del peso. Usare D3DDECLUSAGE \_ BLENDWEIGHT con un indice di utilizzo 0 per specificare i pesi di Blend usati nella combinazione di vertici indicizzati e non indicizzati.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**\_BLENDINDICES D3DDECLUSAGE**
</dt> <dd>

Fusione dei dati degli indici. Usare D3DDECLUSAGE \_ BLENDINDICES con un indice di utilizzo 0 per specificare gli indici di matrice per la funzionalità di skinning con tavolozza indicizzata.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normale**
</dt> <dd>

Dati normali dei vertici. Usare D3DDECLUSAGE \_ Normal con un indice di utilizzo 0 per specificare le normali dei vertici per l'elaborazione del vertice della funzione fissa e l'mosaico n-patch. Usare D3DDECLUSAGE \_ Normal con un indice di utilizzo 1 per specificare le normali dei vertici per l'elaborazione del vertice della funzione fissa per l'interpolazione del vertice.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**\_PSIZE D3DDECLUSAGE**
</dt> <dd>

Dati delle dimensioni del punto. Usare D3DDECLUSAGE \_ PSIZE con un indice di utilizzo 0 per specificare l'attributo di dimensione punto usato dal motore di installazione del rasterizzatore per espandere un punto in un quad per la funzionalità Point-sprite.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**\_TEXCOORD D3DDECLUSAGE**
</dt> <dd>

Dati delle coordinate di trama. Usare D3DDECLUSAGE \_ TEXCOORD, n per specificare le coordinate di trama nell'elaborazione dei vertici delle funzioni fisse e nei pixel shader precedenti a PS \_ 3 \_ 0. Questi possono essere usati per passare dati definiti dall'utente.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**\_Tangente D3DDECLUSAGE**
</dt> <dd>

Dati della tangente del vertice.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE- \_ normale**
</dt> <dd>

Dati binormali vertice.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**\_TESSFACTOR D3DDECLUSAGE**
</dt> <dd>

Singolo valore a virgola mobile positivo. Usare D3DDECLUSAGE \_ TESSFACTOR con un indice di utilizzo 0 per specificare un fattore a mosaico usato nell'unità a mosaico per controllare la frequenza dello schema a mosaico. Per ulteriori informazioni sul tipo di dati, vedere D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**\_Posizione D3DDECLUSAGE**
</dt> <dd>

I dati dei vertici contengono dati di posizione trasformati compresi tra (0, 0) e (larghezza del viewport, altezza del viewport). Usare D3DDECLUSAGE \_ positiont con un indice di utilizzo 0 per specificare la posizione trasformata. Quando viene impostata una dichiarazione contenente questo oggetto, la pipeline non esegue l'elaborazione dei vertici.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Colore D3DDECLUSAGE**
</dt> <dd>

I dati dei vertici contengono il colore speculare o diffuso. Usare il \_ colore D3DDECLUSAGE con un indice di utilizzo 0 per specificare il colore diffuso nel vertex shader della funzione fissa e nei pixel shader precedenti a PS \_ 3 \_ 0. Usare il \_ colore D3DDECLUSAGE con un indice di utilizzo 1 per specificare il colore speculare nel vertex shader della funzione fissa e nei pixel shader precedenti a PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ nebbia**
</dt> <dd>

I dati dei vertici contengono dati di nebbia. Usare D3DDECLUSAGE \_ Fog con un indice di utilizzo 0 per specificare un valore di Blend di nebbia usato dopo il completamento dell'ombreggiatura dei pixel. Si applica ai pixel shader prima della versione PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**\_Profondità D3DDECLUSAGE**
</dt> <dd>

I dati dei vertici contengono dati di profondità.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**\_Esempio D3DDECLUSAGE**
</dt> <dd>

I dati dei vertici contengono dati del campionatore. Usare \_ l'esempio D3DDECLUSAGE con un indice di utilizzo 0 per specificare il valore di spostamento da ricercare. Può essere usato solo con la \_ ricerca D3DDECLUSAGE LOOKUPPRESAMPLED o D3DDECLUSAGE \_ .

</dd> </dl>

## <a name="remarks"></a>Commenti

I dati dei vertici vengono dichiarati con una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Ogni elemento nella matrice contiene un tipo di utilizzo.

Per altre informazioni sulle dichiarazioni dei vertici, vedere [dichiarazione vertici (Direct3D 9)](vertex-declaration.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Dichiarazione vertici (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




