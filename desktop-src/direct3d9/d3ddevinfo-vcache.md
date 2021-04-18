---
description: Hint di ottimizzazione della cache vertex.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Struttura D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322398"
---
# <a name="d3ddevinfo_vcache-structure"></a>\_Struttura D3DDEVINFO VCACHE

Hint di ottimizzazione della cache vertex.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a>Members

<dl> <dt>

**Modello**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Modello di bit. Il valore restituito deve essere FOURCC (' c',' A ',' c',' H ').

</dd> <dt>

**OptMethod**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Metodo di ottimizzazione. Utilizzare 0 per ottenere le strisce più lunghe. Utilizzare 1 per ottimizzare l'utilizzo della cache dei vertici.

</dd> <dt>

**CacheSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni della cache utilizzate come destinazione per l'ottimizzazione. Questa operazione è necessaria solo se OptMethod è 1.

</dd> <dt>

**MagicNumber**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Utilizzato dai metodi di ottimizzazione interni per determinare quando riavviare le strisce. Non può essere impostato o modificato da un utente. Questa operazione è necessaria solo se OptMethod è 1.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
