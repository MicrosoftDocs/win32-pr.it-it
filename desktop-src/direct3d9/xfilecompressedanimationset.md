---
description: Identifica i dati di animazione dei fotogrammi chiave compressi.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Struttura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 41c64ae7bb2ca4acf87e1b63de90f2ccfc78e8d769adf334aa1f68b9bf79de0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518563"
---
# <a name="xfilecompressedanimationset-structure"></a>Struttura XFILECOMPRESSEDANIMATIONSET

Identifica i dati di animazione dei fotogrammi chiave compressi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a>Members

<dl> <dt>

**CompressedBlockSize**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni totali, in byte, dei dati compressi nel buffer dei dati di animazione con fotogrammi chiave compressi.

</dd> <dt>

**TicksPerSec**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di tick dei fotogrammi chiave di animazione che si verificano al secondo.

</dd> <dt>

**Tipo di riproduzione**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo di ciclo di riproduzione del set di animazioni. Vedere [**D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni minime del buffer, in byte, necessarie per contenere i dati di animazione dei fotogrammi chiave compressi. Il valore è uguale a ( ( CompressedBlockSize + 3 ) / 4 ).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
