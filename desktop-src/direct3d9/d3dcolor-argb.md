---
description: Inizializza un colore con i valori alfa, rosso, verde e blu forniti.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354424"
---
# <a name="d3dcolor_argb-macro"></a>D3DCOLOR ( \_ macro ARGB)

Inizializza un colore con i valori alfa, rosso, verde e blu forniti.

## <a name="syntax"></a>Sintassi


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore [D3DCOLOR](d3dcolor.md) che corrisponde ai valori ARGB forniti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_RGBA D3DCOLOR**](d3dcolor-rgba.md)
</dt> <dt>

[**\_Sulle XRGB mentre D3DCOLOR**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




