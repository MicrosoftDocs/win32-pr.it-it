---
description: 'Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math.h): crea una matrice di proiezione prospettica personalizzata con la mano destra.'
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 883ddb49684d4e5f5ca7cfb3585a26653a7f0ef4960b59e3c74aafecdd7e2f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498031"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a>Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math.h)

Compila una matrice di proiezione prospettica personalizzata con la mano destra.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*l* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore x minimo del volume di visualizzazione.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore x massimo del volume di visualizzazione.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore y minimo del volume di visualizzazione.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore y massimo del volume di visualizzazione.

</dd> <dt>

*zn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z minimo del volume di visualizzazione.

</dd> <dt>

*zf* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z massimo del volume di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che è una matrice di proiezione prospettica personalizzata con la mano destra.

## <a name="remarks"></a>Commenti

Tutti i parametri della funzione D3DXMatrixPerspectiveOffCenterRH sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume di visualizzazione.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixPerspectiveOffCenterRH può essere usata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
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

 

 
