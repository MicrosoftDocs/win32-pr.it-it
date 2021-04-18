---
description: Inizializza un colore usando i valori (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV macro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322374"
---
# <a name="d3dcolor_ayuv-macro"></a>D3DCOLOR \_ AYUV-macro

Inizializza un colore usando i valori (a, y, u, v).

## <a name="syntax"></a>Sintassi


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

*y* 
</dt> <dd>

Componente di luminanza del colore. Questo valore deve essere compreso tra 0 e 255.

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

Restituisce il valore [D3DCOLOR](d3dcolor.md) che corrisponde ai valori ARGB forniti.

## <a name="remarks"></a>Commenti

Un colore RGB può essere ridotto a 16 bit per pixel mediante conversione in luminanza e differenze di colore con le equazioni seguenti:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



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

[**\_XYUV D3DCOLOR**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




