---
description: Compila un quaternione con l'imbardata, il pitch e il rullo specificati.
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: Funzione D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d894be61f5f22322f83c4e4a6c6a724de4b9da4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323201"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a>Funzione D3DXQuaternionRotationYawPitchRoll (D3DX10Math. h)

Compila un quaternione con l'imbardata, il pitch e il rullo specificati.

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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.

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

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a una struttura D3DXQUATERNION con l'imbardata, il pitch e il rullo specificati.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXQuaternionRotationYawPitchRoll può essere utilizzata come parametro per un'altra funzione.

Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
