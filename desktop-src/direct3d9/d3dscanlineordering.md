---
description: Flag che indicano il metodo utilizzato dal rasterizzatore per creare un'immagine in una superficie.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumerazione D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323649"
---
# <a name="d3dscanlineordering-enumeration"></a>Enumerazione D3DSCANLINEORDERING

Flag che indicano il metodo utilizzato dal rasterizzatore per creare un'immagine in una superficie.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressive**
</dt> <dd>

L'immagine viene creata dalla prima scanline all'ultima senza alcuna omissione.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ INTERlacciato**
</dt> <dd>

L'immagine viene creata usando il metodo interlacciato, in cui le linee dispari vengono disegnate su passi con numerazione dispari e anche le linee vengono disegnate su passaggi con numero pari.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata come membro in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) e [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




