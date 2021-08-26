---
title: Struttura XMUINT2
description: Descrive un vettore di interi senza segno 2D.
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
ms.openlocfilehash: 39ec30fd4966e46bd511729671c39653640fe3f8f858d74db96e59fa1f09d242
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067271"
---
# <a name="xmuint2-structure"></a>Struttura XMUINT2

Descrive un vettore di interi senza segno 2D.

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

Questa struttura è definita ``D3DX\_DXGIFormatConvert.inl`` nell'intestazione di DirectX SDK (giugno 2010) per l'uso da C++. La versione più recente di questa intestazione in [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package non la definisce più e si basa invece su [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath.



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