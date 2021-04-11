---
description: Viene descritta una tabella di un DC Huffman.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Struttura DXGI_JPEG_DC_HUFFMAN_TABLE (Dxgitype. h)
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
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234991"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>\_Struttura della tabella DXGI JPEG \_ DC \_ Huffman \_

Viene descritta una tabella di un DC Huffman.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
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

 

 




