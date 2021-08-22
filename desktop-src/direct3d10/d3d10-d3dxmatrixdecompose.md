---
description: 'Funzione D3DXMatrixDecompose (D3DX10Math.h): suddivide una matrice di trasformazione 3D generale nei componenti scalari, rotazionali e traslazionali.'
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Funzione D3DXMatrixDecompose (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: be91b4b8ef6b0a18dc7691eb230ae755db31173ab8e42ab8ef0fb105d23630c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498141"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>Funzione D3DXMatrixDecompose (D3DX10Math.h)

Suddivide una matrice di trasformazione 3D generale nei relativi componenti scalari, rotazionali e traslazionali.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOutScale* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore all'oggetto [**D3DXVECTOR3**](d3d10-d3dxvector3.md) di output che contiene i fattori di scala applicati lungo gli assi x, y e z.

</dd> <dt>

*pOutRotation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che descrive la rotazione.

</dd> <dt>

*pOutTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore al vettore D3DXVECTOR3 che descrive la conversione.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore a una matrice [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di input da scomporre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
