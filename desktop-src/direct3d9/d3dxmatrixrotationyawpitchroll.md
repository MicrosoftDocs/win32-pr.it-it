---
description: Compila una matrice con l'imbardata, il pitch e il rullo specificati.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234943"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math. h)

Compila una matrice con l'imbardata, il pitch e il rullo specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Imbardata* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Imbardata intorno all'asse y, in radianti.

</dd> <dt>

*Passo* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Pitch intorno all'asse x, in radianti.

</dd> <dt>

Esegui *rollforward* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ruotare intorno all'asse z, in radianti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) con l'imbardata, il pitch e il rullo specificati.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXMatrixRotationYawPitchRoll** può essere utilizzata come parametro per un'altra funzione.

L'ordine delle trasformazioni è prima di tutto roll, quindi pitch, then imbardata. Rispetto all'asse delle coordinate locali dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.

![illustrazione di roll, pitch e imbardata come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
