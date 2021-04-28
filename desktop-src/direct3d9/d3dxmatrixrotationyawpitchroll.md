---
description: 'Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math.h): compila una matrice con uno yaw, un passo e un lancio specificati.'
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math.h)
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
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118149"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>Funzione D3DXMatrixRotationYawPitchRoll (D3dx9math.h)

Compila una matrice con uno yaw, un passo e un lancio specificati.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Yaw* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Yaw intorno all'asse y, in radianti.

</dd> <dt>

*Tono* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Passo intorno all'asse x, espresso in radianti.

</dd> <dt>

*Roll* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Rullo intorno all'asse z, in radianti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) con yaw, pitch e roll specificati.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixRotationYawPitchRoll** può essere usata come parametro per un'altra funzione.

L'ordine delle trasformazioni è roll first, quindi pitch, quindi yaw. Rispetto all'asse delle coordinate locale dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.

![Illustrazione di rollio, passo e yaw come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



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

 

 
