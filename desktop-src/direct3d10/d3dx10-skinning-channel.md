---
description: Membro della decl del vertice su cui eseguire il Skinning del software. Viene usato con l'API ID3DX10SkinInfo::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Struttura D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235078"
---
# <a name="d3dx10_skinning_channel-structure"></a>\_Struttura del canale di skinning d3dx10 \_

Membro della decl del vertice su cui eseguire il Skinning del software. Viene usato con l'API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Members

<dl> <dt>

**SrcOffset**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di ogni vertice di origine.

</dd> <dt>

**DestOffset**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset dall'inizio di ogni vertice di destinazione.

</dd> <dt>

**Normale**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Determina la matrice di matrici da usare nell'API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) . Se il valore è true, verrà utilizzato *pInverseTransposeBoneMatrices* . in caso contrario, verrà utilizzato *pBoneMatrices* .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
