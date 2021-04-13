---
description: Definisce il metodo di dichiarazione vertex che è un'operazione predefinita eseguita da mosaico (o qualsiasi routine Geometry procedurale sui dati dei vertici durante la suddivisione a mosaico).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumerazione D3DDECLMETHOD (D3D9Types. h)
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
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354384"
---
# <a name="d3ddeclmethod-enumeration"></a>Enumerazione D3DDECLMETHOD

Definisce il metodo di dichiarazione vertex che è un'operazione predefinita eseguita da mosaico (o qualsiasi routine Geometry procedurale sui dati dei vertici durante la suddivisione a mosaico).

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

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**\_Impostazione predefinita D3DDECLMETHOD**
</dt> <dd>

Valore predefinito. Mosaico copia i dati dei vertici (dati spline per le patch) così come sono, senza calcoli aggiuntivi. Quando si usa mosaico, questo elemento è interpolato. In caso contrario, i dati dei vertici vengono copiati nel registro di input. Il tipo di input e di output può essere qualsiasi valore, ma è sempre dello stesso tipo.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ parziali**
</dt> <dd>

Calcola la tangente in un punto della patch rettangolo o triangolo nella direzione U. Il tipo di input può essere uno dei seguenti:

-   \_D3DCOLOR D3DDECLTYPE
-   \_FLOAT3 D3DDECLTYPE
-   \_Float4 D3DDECLTYPE
-   \_SHORT4 D3DDECLTYPE
-   \_UBYTE4 D3DDECLTYPE

Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**\_PARTIALV D3DDECLMETHOD**
</dt> <dd>

Calcola la tangente in un punto della patch rettangolo o triangolo nella direzione V. Il tipo di input può essere uno dei seguenti:

-   \_D3DCOLOR D3DDECLTYPE
-   \_FLOAT3 D3DDECLTYPE
-   \_Float4 D3DDECLTYPE
-   \_SHORT4 D3DDECLTYPE
-   \_UBYTE4 D3DDECLTYPE

Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**\_CROSSUV D3DDECLMETHOD**
</dt> <dd>

Calcola il normale in un punto della patch rettangolo o triangolo prendendo il prodotto incrociato di due tangenti. Il tipo di input può essere uno dei seguenti:

-   \_D3DCOLOR D3DDECLTYPE
-   \_FLOAT3 D3DDECLTYPE
-   \_Float4 D3DDECLTYPE
-   \_SHORT4 D3DDECLTYPE
-   \_UBYTE4 D3DDECLTYPE

Il tipo di output è sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**
</dt> <dd>

Copiare i valori U, V in un punto della patch rettangolo o triangolo. In questo modo si ottiene un valore float 2D. Il tipo di input deve essere impostato su D3DDECLTYPE \_ inutilizzato. Il tipo di dati di output è sempre D3DDECLTYPE \_ FLOAT2. Anche il flusso di input e l'offset sono inutilizzati (ma devono essere impostati su 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**\_Ricerca D3DDECLMETHOD**
</dt> <dd>

Cercare una mappa di spostamento. Il tipo di input può essere uno dei seguenti:

-   \_FLOAT2 D3DDECLTYPE
-   \_FLOAT3 D3DDECLTYPE
-   \_Float4 D3DDECLTYPE

Solo i componenti con estensione x e y vengono usati per la ricerca della mappa di trama. Il tipo di output è sempre D3DDECLTYPE \_ FLOAT1. Il dispositivo deve supportare il mapping di spostamento. Per ulteriori informazioni sul mapping di spostamento, vedere [mapping di spostamento (Direct3D 9)](displacement-mapping.md). Questa costante è supportata solo dalla pipeline programmabile nei dati di N-patch, se N-patch sono abilitate.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**\_LOOKUPPRESAMPLED D3DDECLMETHOD**
</dt> <dd>

Cercare una mappa di spostamento precampionata. Il tipo di input deve essere impostato su D3DDECLTYPE \_ INutilizzato. l'indice del flusso e l'offset del flusso devono essere impostati su 0. Il tipo di output per questa operazione è sempre D3DDECLTYPE \_ FLOAT1. Il dispositivo deve supportare il mapping di spostamento. Per ulteriori informazioni sul mapping di spostamento, vedere [mapping di spostamento (Direct3D 9)](displacement-mapping.md). Questa costante è supportata solo dalla pipeline programmabile nei dati di N-patch, se N-patch sono abilitate. Questo metodo può essere utilizzato solo con l' \_ esempio D3DDECLUSAGE.

</dd> </dl>

## <a name="remarks"></a>Commenti

Mosaico esamina il metodo per determinare i dati da calcolare dai dati dei vertici durante il mosaico. I dati mesh devono usare il valore predefinito. Le patch possono usare qualsiasi altro tipo implementato.

I dati dei vertici vengono dichiarati con una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Ogni elemento nella matrice contiene un metodo di dichiarazione del vertice.

Oltre a usare D3DDECLMETHOD \_ default, una mesh normale può usare \_ i metodi di ricerca D3DDECLMETHOD e D3DDECLMETHOD \_ LOOKUPPRESAMPLED quando N-patch è abilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




