---
title: Struttura XMUINT4
description: Descrive un vettore intero senza segno 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- Struttura XMUINT4 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549896"
---
# <a name="xmuint4-structure"></a>Struttura XMUINT4

Descrive un vettore integer senza segno 4D.

## <a name="syntax"></a>Sintassi


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
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

<dl> <dt>

**z**
</dt> <dd>

Componente z del vettore.

<dl> <dt>

**w**
</dt> <dd>

w-component del vettore.

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a>Commenti

Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione di DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath.




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