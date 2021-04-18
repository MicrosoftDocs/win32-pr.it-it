---
description: Struttura di supporto per la gestione di una tabella di costanti shader. Questa operazione può essere eseguita anche usando ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: Struttura D3DXSHADER_CONSTANTTABLE (D3dx9shader. h)
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
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322594"
---
# <a name="d3dxshader_constanttable-structure"></a>\_Struttura D3DXSHADER CONSTANTTABLE

Struttura di supporto per la gestione di una tabella di costanti shader. Questa operazione può essere eseguita anche usando [**ID3DXConstantTable**](id3dxconstanttable.md).

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

Dimensione della struttura. Vedere la sezione Osservazioni.

</dd> <dt>

**Autore**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio della struttura, in byte, alla stringa che contiene il nome dell'autore.

</dd> <dt>

**Versione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Versione shader.

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

Matrice di informazioni costanti, D3DXSHADER \_ CONSTANTINFO \[ *costanti* \] . Vedere [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).

</dd> <dt>

**Flag**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Flag [D3DXSHADER flag](d3dxshader-flags.md) utilizzati per compilare lo shader.

</dd> <dt>

**Destinazione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset nella stringa che contiene la destinazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni sulla costante dello shader sono incluse in una tabella di commenti delimitati da tabulazioni. Tutti gli offset sono misurati in byte a partire dall'inizio della struttura. Le voci della tabella Constant sono ordinate in base all'autore in ordine crescente.

Una tabella delle costanti shader può essere gestita con le interfacce [**ID3DXConstantTable**](id3dxconstanttable.md) . In alternativa, è possibile gestire la tabella delle costanti con **D3DXSHADER \_ CONSTANTTABLE**.

Questo membro di dimensione viene spesso inizializzato usando quanto segue:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
