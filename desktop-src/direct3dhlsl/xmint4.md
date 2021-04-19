---
title: Struttura XMINT4
description: Descrive un vettore di Integer 4D.
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
ms.openlocfilehash: d532f3a2a2332874f7b7c22f17992c22984e3f86
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222839"
---
# <a name="xmint4-structure"></a>Struttura XMINT4

Descrive un vettore di Integer 4D.

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

componente x del vettore.

</dd> <dt>

**y**
</dt> <dd>

componente y del vettore.

<dl> <dt>

**z**
</dt> <dd>

componente z del vettore.

<dl> <dt>

**w**
</dt> <dd>

componente w del vettore.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="remarks"></a>Commenti

Questa struttura è definita nell' ``D3DX\_DXGIFormatConvert.inl`` intestazione in DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX:: XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath.



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture](format-conversion-structures.md)
</dt> <dt>

[Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
