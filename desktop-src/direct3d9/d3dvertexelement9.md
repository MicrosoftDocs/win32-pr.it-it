---
description: Definisce il layout dei dati dei vertici. Ogni vertice può contenere uno o più tipi di dati e ogni tipo di dati è descritto da un elemento vertice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Struttura D3DVERTEXELEMENT9 (D3D9Types.h)
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
ms.openlocfilehash: cda5b92170ef21f7bb66233f0748afe0c780837bbcb0eee9ef3c970880070422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527295"
---
# <a name="d3dvertexelement9-structure"></a>Struttura D3DVERTEXELEMENT9

Definisce il layout dei dati dei vertici. Ogni vertice può contenere uno o più tipi di dati e ogni tipo di dati è descritto da un elemento vertice.

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

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di flusso.

</dd> <dt>

**Offset**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio dei dati dei vertici ai dati associati al tipo di dati specifico.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo di dati, specificato come [**D3DDECLTYPE.**](./d3ddecltype.md) Uno dei diversi tipi predefiniti che definiscono le dimensioni dei dati. Alcuni metodi hanno un tipo implicito.

</dd> <dt>

**Metodo**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Il metodo specifica l'elaborazione a tessellatore, che determina il modo in cui il tessellatore interpreta (o opera) i dati dei vertici. Per altre informazioni, vedere [**D3DDECLMETHOD.**](./d3ddeclmethod.md)

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Definisce l'oggetto per cui verranno usati i dati. l'interoperabilità tra i layout dei dati dei vertici e i vertex shader. Ogni utilizzo agisce per associare una dichiarazione di vertice a un vertex shader. In alcuni casi, hanno un'interpretazione speciale. Ad esempio, un elemento che specifica D3DDECLUSAGE NORMAL o \_ D3DDECLUSAGE POSITION viene usato dal tessellatore di patch N per configurare la rappresentazione a più \_ livelli. Per un elenco della semantica disponibile, vedere [**D3DDECLUSAGE.**](./d3ddeclusage.md) D3DDECLUSAGE TEXCOORD può essere usato per i campi definiti dall'utente (per i quali non è definito \_ un utilizzo esistente).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Modifica i dati di utilizzo per consentire all'utente di specificare più tipi di utilizzo.

</dd> </dl>

## <a name="remarks"></a>Commenti

I dati dei vertici vengono definiti usando una matrice **di strutture D3DVERTEXELEMENT9.** Usare [**D3DDECL \_ END**](d3ddecl-end.md) per dichiarare l'ultimo elemento nella dichiarazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Dichiarazione vertice (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
