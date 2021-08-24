---
description: Inizializza un colore con i valori a virgola mobile rosso, verde, blu e alfa forniti.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751231"
---
# <a name="d3dcolor_colorvalue-macro"></a>Macro D3DCOLOR \_ COLORVALUE

Inizializza un colore con i valori a virgola mobile rosso, verde, blu e alfa forniti.

## <a name="syntax"></a>Sintassi


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*r* 
</dt> <dd>

Componente rosso del colore. Questo valore deve essere un valore a virgola mobile compreso nell'intervallo compreso tra 0,0 e 1,0.

</dd> <dt>

*G* 
</dt> <dd>

Componente verde del colore. Questo valore deve essere un valore a virgola mobile compreso nell'intervallo compreso tra 0,0 e 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Componente blu del colore. Questo valore deve essere un valore a virgola mobile compreso nell'intervallo compreso tra 0,0 e 1,0.

</dd> <dt>

*Un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere un valore a virgola mobile compreso nell'intervallo compreso tra 0,0 e 1,0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il [**valore D3DCOLOR**](d3dcolor.md) che corrisponde ai valori RGBA forniti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




