---
description: Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'Metodo ID3DXBaseMesh:: GenerateAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401996"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>Metodo ID3DXBaseMesh:: GenerateAdjacency

Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Epsilon* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Specifica che i vertici che differiscono dalla posizione minore di Epsilon devono essere considerati coincidenti.

</dd> <dt>

*pAdjacency* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per volto da riempire con gli indici di visi adiacenti. Il numero di byte in questa matrice deve essere almeno 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno.

L'ordine delle voci nel buffer adiacenza è determinato dall'ordine degli indici dei vertici nel buffer dell'indice. Il triangolo adiacente 0 corrisponde sempre al bordo tra gli indici degli angoli 0 e 1. Il triangolo adiacente 1 corrisponde sempre al bordo tra gli indici degli angoli 1 e 2, mentre il triangolo adiacente 2 corrisponde al bordo tra gli indici degli angoli 2 e 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh:: OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
