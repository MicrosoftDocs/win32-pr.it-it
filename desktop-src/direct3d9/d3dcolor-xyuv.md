---
description: Inizializza un colore con i valori (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: D3DCOLOR_XYUV macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: caa6bc1eb9586c1526a7af674040fd703ff0a75a5055ce42e13378206e82c879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300325"
---
# <a name="d3dcolor_xyuv-macro"></a>Macro D3DCOLOR \_ XYUV

Inizializza un colore con i valori (y, u, v).

## <a name="syntax"></a>Sintassi


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*y* 
</dt> <dd>

Componente Luminance del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*u* 
</dt> <dd>

Luminosità blu del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*v* 
</dt> <dd>

Luminosità rossa del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**valore D3DCOLOR**](d3dcolor.md) che corrisponde ai valori (y, u, v) forniti.

## <a name="remarks"></a>Commenti

Un colore RGB può essere ridotto a 16 bit per pixel conversione in luminance e differenze di colore con le equazioni seguenti:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



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

[**D3DCOLOR \_ AYUV**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




