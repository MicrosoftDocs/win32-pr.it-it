---
description: Definisce il layout dei dati del vertice. Ogni vertice può contenere uno o più tipi di dati e ogni tipo di dati è descritto da un elemento vertice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Struttura D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323027"
---
# <a name="d3dvertexelement9-structure"></a>Struttura D3DVERTEXELEMENT9

Definisce il layout dei dati del vertice. Ogni vertice può contenere uno o più tipi di dati e ogni tipo di dati è descritto da un elemento vertice.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>Members

<dl> <dt>

**Stream**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di flusso.

</dd> <dt>

**Offset**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio dei dati dei vertici ai dati associati al tipo di dati specifico.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo di dati, specificato come [**D3DDECLTYPE**](./d3ddecltype.md). Uno dei diversi tipi predefiniti che definiscono le dimensioni dei dati. Alcuni metodi hanno un tipo implicito.

</dd> <dt>

**Metodo**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Il metodo specifica l'elaborazione mosaico, che determina il modo in cui mosaico interpreta o opera sui dati dei vertici. Per ulteriori informazioni, vedere [**D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Definisce gli elementi per i quali verranno utilizzati i dati. ovvero l'interoperabilità tra layout di dati dei vertici e vertex shader. Ogni utilizzo agisce per associare una dichiarazione di vertice a un vertex shader. In alcuni casi, hanno un'interpretazione speciale. Ad esempio, un elemento che specifica \_ la posizione normale o D3DDECLUSAGE \_ di D3DDECLUSAGE viene usato da N-patch mosaico per impostare lo schema a mosaico. Per un elenco della semantica disponibile, vedere [**D3DDECLUSAGE**](./d3ddeclusage.md) . D3DDECLUSAGE \_ TEXCOORD può essere usato per i campi definiti dall'utente (che non hanno un utilizzo esistente definito).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Modifica i dati di utilizzo per consentire all'utente di specificare più tipi di utilizzo.

</dd> </dl>

## <a name="remarks"></a>Commenti

I dati dei vertici vengono definiti mediante una matrice di strutture **D3DVERTEXELEMENT9** . Usare [**D3DDECL \_ end**](d3ddecl-end.md) per dichiarare l'ultimo elemento nella dichiarazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Dichiarazione vertici (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
