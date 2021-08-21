---
description: Crea una nuova mesh di patch con la dichiarazione di vertice specificata.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: Metodo ID3DXPatchMesh::CloneMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1418bf890ae0ba10adec9e0c7de74eb5f118f91566554eb325cc2badaedfc613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294382"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>Metodo ID3DXPatchMesh::CloneMesh

Crea una nuova mesh di patch con la dichiarazione di vertice specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [**flag D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.

</dd> <dt>

*pDecl* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che specificano il formato del vertice per i vertici nella mesh di output.

</dd> <dt>

*pMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXPatchMesh**](id3dxpatchmesh.md) che rappresenta la mesh clonata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

**CloneMesh** converte il buffer dei vertici nella nuova dichiarazione di vertice. Le voci nella dichiarazione del vertice nuove alla mesh originale vengono impostate su 0. Se la mesh corrente ha adienza, anche la nuova mesh avrà adienza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
