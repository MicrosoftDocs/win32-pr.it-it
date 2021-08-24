---
title: Struttura XMINT4
description: Descrive un vettore integer 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- Struttura XMINT4 HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c926d382cf9746a9a9a5603077d9bf4423dbf33368d471809108c584a7d748dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119369101"
---
# <a name="xmint4-structure"></a>Struttura XMINT4

Descrive un vettore integer 4D.

## <a name="syntax"></a>Sintassi


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="remarks"></a>Commenti

Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione in DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione nel pacchetto di NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath.



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture](format-conversion-structures.md)
</dt> <dt>

[Decompressione e impacchettamento del formato DXGI \_ per la In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>