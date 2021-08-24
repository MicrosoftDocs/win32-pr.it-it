---
title: Struttura XMINT2
description: Descrive un vettore integer 2D.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- Struttura XMINT2 HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc613cd87b212ca21aacf1744b7789bd49732a555630d5cfc6051eaab2b3d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484181"
---
# <a name="xmint2-structure"></a>Struttura XMINT2

Descrive un vettore integer 2D.

## <a name="syntax"></a>Sintassi


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
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

Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione di DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione in [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package non la definisce più e si basa invece su [DirectX::XMINT2](/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath.



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture](format-conversion-structures.md)
</dt> <dt>

[Decompressione e creazione di un pacchetto DXGI \_ FORMAT per la In-Place delle immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>