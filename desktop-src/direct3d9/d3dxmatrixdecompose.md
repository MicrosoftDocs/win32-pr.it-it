---
description: 'Funzione D3DXMatrixDecompose (D3dx9math.h): suddivide una matrice di trasformazione 3D generale nei relativi componenti scalari, rotazionali e traslazionali.'
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Funzione D3DXMatrixDecompose (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aaaa1059c4ffeafa453694d9c348656c856decaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098189"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a>Funzione D3DXMatrixDecompose (D3dx9math.h)

Suddivide una matrice di trasformazione 3D generale nei relativi componenti scalari, rotazionali e traslazionali.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOutScale* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore all'oggetto [**D3DXVECTOR3**](d3dxvector3.md) di output che contiene i fattori di scala applicati lungo gli assi x, y e z.

</dd> <dt>

*pOutRotation* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione.

</dd> <dt>

*pOutTranslation* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore al [**vettore D3DXVECTOR3**](d3dxvector3.md) che descrive la conversione.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una matrice [**D3DXMATRIX**](d3dxmatrix.md) di input da scomporre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




