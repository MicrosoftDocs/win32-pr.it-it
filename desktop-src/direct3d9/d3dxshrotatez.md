---
description: Ruota il vettore armonico sferico (SH) nell'asse z in base all'angolo specificato.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Funzione D3DXSHRotateZ (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401957"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a>Funzione D3DXSHRotateZ (D3dx9math. h)

Ruota il vettore armonico sferico (SH) nell'asse z in base all'angolo specificato.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output armonici sferici (SH). La valutazione genera coefficienti Order ². Questo puntatore non deve avere alias con *pin*. Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*Angolo* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Angolo di rotazione, in radianti. La rotazione viene eseguita intorno all'asse z.

</dd> <dt>

*Aggiungi* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore ai coefficienti SH ruotati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:

-   l è il grado della funzione di base.
-   m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Trasferimento Radiance pre-calcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
