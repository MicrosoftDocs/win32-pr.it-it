---
description: 'Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math.h): compila una matrice con un yaw, un passo e un rollio specificati.'
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108949"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a>Funzione D3DXMatrixRotationYawPitchRoll (D3DX10Math.h)

Compila una matrice con uno yaw, un passo e un rollio specificati.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Yaw* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Yaw intorno all'asse y, in radianti.

</dd> <dt>

*Pitch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Passo intorno all'asse x, in radianti.

</dd> <dt>

*Roll* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Eseguire il roll-around dell'asse z, in radianti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX con lo yaw, il passo e il rollio specificati.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixRotationYawPitchRoll può essere usata come parametro per un'altra funzione.

L'ordine delle trasformazioni è roll first, quindi pitch e yaw. Rispetto all'asse delle coordinate locale dell'oggetto, equivale alla rotazione intorno all'asse z, seguita dalla rotazione intorno all'asse x, seguita dalla rotazione intorno all'asse y, come illustrato nella figura seguente.

![illustrazione di lancio, passo e yaw come rotazioni intorno ai tre assi](images/pitchyawroll.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
