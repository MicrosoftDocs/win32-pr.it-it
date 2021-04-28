---
description: "Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math.h): compila un quaternione con l'yaw, il passo e il lancio dati."
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117999"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a>Funzione D3DXQuaternionRotationYawPitchRoll (D3dx9math.h)

Compila un quaternione con l'yaw, il passo e il lancio dati.

## <a name="syntax"></a>Sintassi


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) con yaw, pitch e roll specificati.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXQuaternionRotationYawPitchRoll** può essere usata come parametro per un'altra funzione.

Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
