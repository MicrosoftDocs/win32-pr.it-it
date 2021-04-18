---
description: Identifica i dati di animazione del fotogramma chiave compressi.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Struttura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh. h)
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
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322294"
---
# <a name="xfilecompressedanimationset-structure"></a>Struttura XFILECOMPRESSEDANIMATIONSET

Identifica i dati di animazione del fotogramma chiave compressi.

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

Dimensioni totali, in byte, dei dati compressi nel buffer dei dati di animazione del fotogramma chiave compresso.

</dd> <dt>

**TicksPerSec**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di cicli del fotogramma chiave di animazione che si verificano al secondo.

</dd> <dt>

**PlaybackType**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Tipo del ciclo di riproduzione del set di animazioni. Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).

</dd> <dt>

**BufferLength**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni minime del buffer, in byte, necessarie per conservare i dati di animazione del fotogramma chiave compressi. Il valore è uguale a ((CompressedBlockSize + 3)/4).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di file D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
