---
description: Definisce il metodo di dichiarazione dei vertici, che è un'operazione predefinita eseguita dal tessellatore (o da qualsiasi routine geometrica procedurale sui dati dei vertici durante la tessellazione).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumerazione D3DDECLMETHOD (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f34700666ecb830470e58a3f3389cd6207be68403e612f50ddafc841dd839ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565061"
---
# <a name="d3ddeclmethod-enumeration"></a>Enumerazione D3DDECLMETHOD

Definisce il metodo di dichiarazione dei vertici, che è un'operazione predefinita eseguita dal tessellatore (o da qualsiasi routine geometrica procedurale sui dati dei vertici durante la tessellazione).

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ DEFAULT**
</dt> <dd>

Valore predefinito. Il tessellatore copia i dati dei vertici (dati spline per le patch) così come sono, senza calcoli aggiuntivi. Quando viene usato il tessellatore, questo elemento viene interpolato. In caso contrario, i dati dei vertici vengono copiati nel registro di input. Il tipo di input e di output può essere qualsiasi valore, ma sono sempre dello stesso tipo.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**
</dt> <dd>

Calcola la tangente in un punto del rettangolo o del triangolo in direzione U. Il tipo di input può essere uno dei seguenti:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

Calcola la tangente in un punto del rettangolo o del triangolo nella direzione V. Il tipo di input può essere uno dei seguenti:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

Calcola la normale in un punto del rettangolo o del triangolo prendendo il prodotto incrociato di due tangenti. Il tipo di input può essere uno dei seguenti:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**
</dt> <dd>

Copiare i valori U, V in un punto del rettangolo o della patch del triangolo. Il risultato è un float 2D. Il tipo di input deve essere impostato su D3DDECLTYPE \_ UNUSED. Il tipo di dati di output è sempre D3DDECLTYPE \_ FLOAT2. Anche il flusso di input e l'offset sono inutilizzati (ma devono essere impostati su 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**RICERCA D3DDECLMETHOD \_**
</dt> <dd>

Cercare una mappa di spostamento. Il tipo di input può essere uno dei seguenti:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

Per la ricerca della mappa delle trame vengono usati solo i componenti .x e .y. Il tipo di output è sempre D3DDECLTYPE \_ FLOAT1. Il dispositivo deve supportare il mapping dello spostamento. Per altre informazioni sul mapping dello spostamento, vedere [Mapping spostamento (Direct3D 9).](displacement-mapping.md) Questa costante è supportata solo dalla pipeline programmabile sui dati con N patch, se sono abilitate N patch.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

Cercare una mappa di spostamento precampionata. Il tipo di input deve essere impostato su D3DDECLTYPE UNUSED. L'indice del flusso e l'offset del flusso \_ devono essere impostati su 0. Il tipo di output per questa operazione è sempre D3DDECLTYPE \_ FLOAT1. Il dispositivo deve supportare il mapping dello spostamento. Per altre informazioni sul mapping dello spostamento, vedere [Mapping spostamento (Direct3D 9).](displacement-mapping.md) Questa costante è supportata solo dalla pipeline programmabile sui dati con N patch, se sono abilitate N patch. Questo metodo può essere usato solo con D3DDECLUSAGE \_ SAMPLE.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tessellatore esamina il metodo per determinare quali dati calcolare dai dati dei vertici durante la tessellazione. I dati mesh devono usare il valore predefinito. Le patch possono usare qualsiasi altro tipo implementato.

I dati dei vertici vengono dichiarati con una matrice [**di strutture D3DVERTEXELEMENT9.**](d3dvertexelement9.md) Ogni elemento nella matrice contiene un metodo di dichiarazione del vertice.

Oltre a usare D3DDECLMETHOD DEFAULT, una mesh normale può usare i metodi \_ D3DDECLMETHOD LOOKUP e \_ D3DDECLMETHOD LOOKUPPRESAMPLED quando sono abilitate \_ le patch N.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




