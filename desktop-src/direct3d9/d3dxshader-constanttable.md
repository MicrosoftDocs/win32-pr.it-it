---
description: Struttura dell'helper per la gestione di una tabella costante shader. Questa operazione può essere eseguita anche usando ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE struttura (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027291"
---
# <a name="d3dxshader_constanttable-structure"></a>Struttura D3DXSHADER \_ CONSTANTTABLE

Struttura dell'helper per la gestione di una tabella costante shader. Questa operazione può essere eseguita anche [**usando ID3DXConstantTable.**](id3dxconstanttable.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni della struttura . Vedere la sezione Osservazioni.

</dd> <dt>

**Autore**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di questa struttura , in byte, alla stringa che contiene il nome dell'autore.

</dd> <dt>

**Version**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Versione dello shader.

</dd> <dt>

**Costanti**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di costanti.

</dd> <dt>

**ConstantInfo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matrice di informazioni costanti, costanti D3DXSHADER \_ CONSTANTINFO \[  \] . Vedere [**D3DXSHADER \_ CONSTANTINFO.**](d3dxshader-constantinfo.md)

</dd> <dt>

**Flag**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Flag [D3DXSHADER usati](d3dxshader-flags.md) per compilare lo shader.

</dd> <dt>

**Destinazione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset nella stringa che contiene la destinazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni sulle costanti shader sono incluse in una tabella di commenti delimitata da tabulazioni. Tutti gli offset vengono misurati in byte dall'inizio della struttura . Le voci nella tabella delle costanti vengono ordinate in base a Creator in ordine crescente.

Una tabella costante shader può essere gestita con le [**interfacce ID3DXConstantTable.**](id3dxconstanttable.md) In alternativa, è possibile gestire la tabella delle costanti **con D3DXSHADER \_ CONSTANTTABLE.**

Questo membro di dimensione viene spesso inizializzato usando quanto segue:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
