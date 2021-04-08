---
description: Inizializza un colore con i valori a virgola mobile rosso, verde, blu e alfa forniti.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE macro (D3d9types. h)
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
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761956"
---
# <a name="d3dcolor_colorvalue-macro"></a>D3DCOLOR \_ COLORVALUE-macro

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

Componente rosso del colore. Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del colore. Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Componente blu del colore. Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.

</dd> <dt>

*un* 
</dt> <dd>

Componente alfa del colore. Questo valore deve essere un valore a virgola mobile compreso tra 0,0 e 1,0.

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
</dt> </dl>

 

 




