---
title: Struttura XMUINT2
description: Descrive un vettore integer senza segno 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- Struttura XMUINT2 HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549566"
---
# <a name="xmuint2-structure"></a>Struttura XMUINT2

Descrive un vettore integer senza segno 2D.

## <a name="syntax"></a>Sintassi


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

Componente x del vettore.

</dd> <dt>

**y**
</dt> <dd>

Componente y del vettore.

</dd> </dl>



## <a name="remarks"></a>Commenti

Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione in DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath.



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture](format-conversion-structures.md)
</dt> <dt>

[Decompressione e impacchettamento del formato DXGI \_ per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>