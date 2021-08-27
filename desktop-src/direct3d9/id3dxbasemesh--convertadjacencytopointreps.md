---
description: Converte le informazioni di adicenza della mesh in una matrice di rappresentanti di punti.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: Metodo ID3DXBaseMesh::ConvertAdjacencyToPointReps (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 729e6b67c68f5a9560cbf0aeab5d8f28b72854be49ebc00fb0f0924a5afa4b38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096031"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a>Metodo ID3DXBaseMesh::ConvertAdjacencyToPointReps

Converte le informazioni di adicenza della mesh in una matrice di rappresentanti di punti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAdjacency* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh. Il numero di byte in questa matrice deve essere almeno \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).

</dd> <dt>

*pPRep* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di un valore DWORD per vertice della mesh che verrà riempita con dati rappresentativi del punto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
