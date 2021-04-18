---
description: Descrive una tabella di Huffman AC JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Struttura DXGI_JPEG_AC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322520"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>\_Struttura della \_ \_ tabella Huffman AC DXGI JPEG \_

Descrive una tabella di Huffman AC JPEG.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**Codecounts**
</dt> <dd>

Numero di codici per ogni lunghezza del codice.

</dd> <dt>

**Codevalues**
</dt> <dd>

Valori del codice del Huffman, in ordine di aumento della lunghezza del codice.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




