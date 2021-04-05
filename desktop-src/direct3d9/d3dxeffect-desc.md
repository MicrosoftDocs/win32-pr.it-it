---
description: Descrive un oggetto effetto.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Struttura D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762053"
---
# <a name="d3dxeffect_desc-structure"></a>\_Struttura D3DXEFFECT DESC

Descrive un oggetto effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Autore**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Stringa che contiene il nome dell'autore dell'effetto.

</dd> <dt>

**Parametri**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di parametri utilizzati per effetto.

</dd> <dt>

**Tecniche**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di tecniche che consentono di eseguire il rendering dell'effetto.

</dd> <dt>

**Funzioni**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di funzioni che possono eseguire il rendering dell'effetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un oggetto Effect può contenere più tecniche di rendering e parametri per lo stesso effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
