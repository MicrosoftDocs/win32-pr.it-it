---
description: Inizializza un colore con i valori rosso, verde, blu e alfa forniti.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: D3DCOLOR_RGBA macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322372"
---
# <a name="d3dcolor_rgba-macro"></a>D3DCOLOR \_ RGBA-macro

Inizializza un colore con i valori rosso, verde, blu e alfa forniti.

## <a name="syntax"></a>Sintassi


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*r* 
</dt> <dd>

Componente rosso del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente blu del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore [**D3DCOLOR**](d3dcolor.md) che corrisponde ai valori RGBA forniti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**\_Sulle XRGB mentre D3DCOLOR**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




