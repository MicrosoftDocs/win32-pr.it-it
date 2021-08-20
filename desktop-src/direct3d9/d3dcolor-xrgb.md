---
description: Inizializza un colore con i valori rosso, verde e blu specificati.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: D3DCOLOR_XRGB macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: a31801236720d0a01eefe7f41ac6bd260c1364bb81c437cf6a85088c1c022b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527601"
---
# <a name="d3dcolor_xrgb-macro"></a>Macro D3DCOLOR \_ XRGB

Inizializza un colore con i valori rosso, verde e blu specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*r* 
</dt> <dd>

Componente rosso del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*G* 
</dt> <dd>

Componente verde del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente blu del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**valore D3DCOLOR**](d3dcolor.md) che corrisponde ai valori RGB forniti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> </dl>

 

 




