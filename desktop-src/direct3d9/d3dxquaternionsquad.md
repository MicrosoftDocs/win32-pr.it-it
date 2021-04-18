---
description: Esegue l'interpolazione tra quaternioni usando l'interpolazione quadrangolare sferica.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Funzione D3DXQuaternionSquad (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322486"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a>Funzione D3DXQuaternionSquad (D3dx9math. h)

Esegue l'interpolazione tra quaternioni usando l'interpolazione quadrangolare sferica.

## <a name="syntax"></a>Sintassi


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pQ1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.

</dd> <dt>

*PA* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.

</dd> <dt>

*PB* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.

</dd> <dt>

*computer* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parametro che indica la distanza di interpolazione tra i quaternioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'interpolazione quadrangolare sferica.

## <a name="remarks"></a>Commenti

Questa funzione usa la sequenza di operazioni di interpolazione lineare sferica seguente:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXQuaternionSquad** può essere utilizzata come parametro per un'altra funzione.

Per un esempio di interpolazione tra quaternioni, vedere l'esempio SkinnedMesh. È possibile ottenere questo esempio e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionExp**](d3dxquaternionexp.md)
</dt> <dt>

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
