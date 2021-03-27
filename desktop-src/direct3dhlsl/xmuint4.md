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
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982097"
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

 

 





