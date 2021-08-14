---
description: Inizializza un colore usando i valori (a,y,u,v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV macro (D3d9types.h)
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
ms.openlocfilehash: 5e1900bf0d400971786eb37dd5138154913562982e1a1e3221c8002ac51fbf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300315"
---
# <a name="d3dcolor_ayuv-macro"></a>Macro AYUV D3DCOLOR \_

Inizializza un colore usando i valori (a,y,u,v).

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

*Un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere compreso nell'intervallo compreso tra 0 e 255.

</dd> <dt>

*y* 
</dt> <dd>

Componente Luminance del colore. Questo valore deve essere compreso nell'intervallo compreso tra 0 e 255.

</dd> <dt>

*u* 
</dt> <dd>

Luminosità blu del colore. Questo valore deve essere compreso nell'intervallo compreso tra 0 e 255.

</dd> <dt>

*v* 
</dt> <dd>

Luminosità rossa del colore. Questo valore deve essere compreso nell'intervallo compreso tra 0 e 255.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [valore D3DCOLOR](d3dcolor.md) che corrisponde ai valori ARGB forniti.

## <a name="remarks"></a>Commenti

Un colore RGB può essere ridotto a 16 bit per pixel tramite la conversione alla luminanza e alle differenze di colore con le equazioni seguenti:


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

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




