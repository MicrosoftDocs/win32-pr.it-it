---
description: Inizializza un colore con i valori (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: D3DCOLOR_XYUV macro (D3d9types. h)
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
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886271"
---
# <a name="d3dcolor_xyuv-macro"></a>D3DCOLOR \_ XYUV-macro

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

Restituisce il valore [**D3DCOLOR**](d3dcolor.md) che corrisponde ai valori specificati (y, u, v).

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

[**\_AYUV D3DCOLOR**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




