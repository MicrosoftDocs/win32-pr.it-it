---
description: 'Funzione D3DXMatrixOrthoLH (D3DX10Math.h): crea una matrice di proiezione ortogonale mancino.'
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Funzione D3DXMatrixOrthoLH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b8b1b64818f4c0903897dc5b1de83b1aaa963461e909edbbfc9ba8dc4a1f10f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282961"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a>Funzione D3DXMatrixOrthoLH (D3DX10Math.h)

Compila una matrice di proiezione ortogonale mancino.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Larghezza del volume di visualizzazione.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Altezza del volume di visualizzazione.

</dd> <dt>

*zn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z minimo del volume di visualizzazione, definito z-near.

</dd> <dt>

*zf* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z massimo del volume di visualizzazione, definito z-far.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Commenti

Tutti i parametri della funzione D3DXMatrixOrthoLH sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume di visualizzazione.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixOrthoLH può essere usata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
