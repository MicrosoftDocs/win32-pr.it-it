---
description: Ottiene le dimensioni della mesh a tessellazione, dato un livello a trama.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: Metodo ID3DXPatchMesh::GetTessSize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4668f50236684f104aedf0ad9ecad413a583facbc45d5f3fa0331abb5938bf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493051"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>Metodo ID3DXPatchMesh::GetTessSize

Ottiene le dimensioni della mesh a tessellazione, dato un livello a trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTessLevel* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Livello a tessellazione.

</dd> <dt>

*Adattivo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

A tessitori adattivi. Per lo schema a più livelli adattivo, impostare questo valore su **TRUE** e impostare fTessLevel sul valore massimo. Ciò comporterà la dimensione massima della mesh necessaria per la trama adattiva.

</dd> <dt>

*NumTriangles* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di triangoli generati dalla mesh a scorrimento.

</dd> <dt>

*NumVertices* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di vertici generati dalla mesh a tessella.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo presuppone una struttura a tessitori uniforme.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
