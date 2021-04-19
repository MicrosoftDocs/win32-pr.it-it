---
title: Struttura XMINT2
description: Descrive un vettore di interi 2D.
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
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222859"
---
# <a name="xmint2-structure"></a>Struttura XMINT2

Descrive un vettore di interi 2D.

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

componente x del vettore.

</dd> <dt>

**y**
</dt> <dd>

componente y del vettore.

</dd> </dl>



## <a name="remarks"></a>Commenti

Questa struttura è definita nell' ``D3DX\_DXGIFormatConvert.inl`` intestazione in DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath.



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture](format-conversion-structures.md)
</dt> <dt>

[Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
