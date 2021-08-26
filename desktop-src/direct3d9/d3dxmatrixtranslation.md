---
description: Compila una matrice utilizzando gli offset specificati.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: Funzione D3DXMatrixTranslation (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6aaa14bbd2f82be7ac87857c05a863b6459440dcfdd383d2144fe1b4426019ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986521"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a>Funzione D3DXMatrixTranslation (D3dx9math.h)

Compila una matrice utilizzando gli offset specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Offset della coordinata X.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Offset della coordinata Y.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Offset della coordinata Z.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una [**struttura D3DXMATRIX**](d3dxmatrix.md) che contiene una matrice di trasformazione tradotta.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, D3DXMATRIXTranslation può essere usato come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
