---
description: Segnala il numero di triangoli elaborati e ritagliati dall'elaborazione dei vertici software del runtime.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: D3DDEVINFO_D3DVERTEXSTATS struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80edbdcdeea5df6ff020c0c4cc2179db5152c15cc4965efe6580db7fd7bdcc48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894531"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>Struttura D3DDEVINFO \_ D3DVERTEXSTATS

Segnala il numero di triangoli elaborati e ritagliati dall'elaborazione dei vertici software del runtime.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero totale di triangoli che non vengono ritagliati in questo frame.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di nuovi triangoli generati dal ritaglio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare il runtime di debug e l'elaborazione dei vertici software per ottenere il numero di primitive non ritagliate e ritagliate per una determinata scena. Le primitive vengono in genere ritagliate in base a una banda di protezione (se presente). La banda di protezione di ritaglio è impostata con parametri come GuardBandLeft in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
