---
description: Inizializza un colore con i valori alfa, rosso, verde e blu specificati.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB macro (D3d9types.h)
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
ms.openlocfilehash: 8b65ae82673e98d666754ae42348cb62b3c336a1e642a5f78607924dc58313dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805431"
---
# <a name="d3dcolor_argb-macro"></a>Macro ARGB D3DCOLOR \_

Inizializza un colore con i valori alfa, rosso, verde e blu specificati.

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

*Un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere compreso tra 0 e 255.

</dd> <dt>

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

Restituisce il [valore D3DCOLOR](d3dcolor.md) che corrisponde ai valori ARGB forniti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




