---
description: Flag che indicano il metodo utilizzato dal rasterizzatore per creare un'immagine su una superficie.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumerazione D3DSCANLINEORDERING (D3d9types.h)
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
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987231"
---
# <a name="d3dscanlineordering-enumeration"></a>Enumerazione D3DSCANLINEORDERING

Flag che indicano il metodo utilizzato dal rasterizzatore per creare un'immagine su una superficie.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ PROGRESSIVO**
</dt> <dd>

L'immagine viene creata dalla prima riga di analisi all'ultima senza ignorare alcuna.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ INTERLACED**
</dt> <dd>

L'immagine viene creata usando il metodo interlacciato in cui le linee dispari vengono disegnate su passaggi dispari e le linee pari vengono disegnate su passaggi pari.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata come membro in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) e [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




