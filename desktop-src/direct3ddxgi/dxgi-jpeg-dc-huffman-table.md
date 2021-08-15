---
description: Descrive una tabella JPEG DC huffman.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE struttura (Dxgitype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b431bbccb66bcb24e068229493ef87f2ac96736161bb306609ac4dd479dfb7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987121"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>Struttura DXGI \_ JPEG \_ DC \_ HUFFMAN \_ TABLE

Descrive una tabella JPEG DC huffman.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**CodeCounts**
</dt> <dd>

Numero di codici per ogni lunghezza del codice.

</dd> <dt>

**CodeValues**
</dt> <dd>

Valori di codice Huffman, in ordine di aumento della lunghezza del codice.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dxgitype.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




