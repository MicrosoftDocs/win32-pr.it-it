---
title: Struttura XMUINT4
description: Descrive un vettore di Unsigned Integer 4D.
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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222849"
---
# <a name="xmuint4-structure"></a>Struttura XMUINT4

Descrive un vettore di Unsigned Integer 4D.

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




## <a name="remarks"></a>Commenti

Questa struttura è definita nell' ``D3DX\_DXGIFormatConvert.inl`` intestazione in DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione nel pacchetto NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) non la definisce più e si basa invece su [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath.




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
