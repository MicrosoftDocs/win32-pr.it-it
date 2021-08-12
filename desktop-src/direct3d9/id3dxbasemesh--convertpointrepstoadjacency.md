---
description: Converte i dati rappresentativi dei punti in informazioni sull'adicenza della mesh.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: Metodo ID3DXBaseMesh::ConvertPointRepsToAdjacency (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b888bc7fe8be0aa8bbac1150717ff90440bb797d84d910f7bcb6ee4f35f49345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296209"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a>Metodo ID3DXBaseMesh::ConvertPointRepsToAdjacency

Converte i dati rappresentativi dei punti in informazioni sull'adicenza della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPRep* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di un valore DWORD per vertice della mesh che contiene dati rappresentativi del punto. Questo parametro è facoltativo. Se si specifica **un valore NULL,** questo parametro verrà interpretato come matrice "identity".

</dd> <dt>

*pAdjacency* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh. Il numero di byte in questa matrice deve essere almeno \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).

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

 

 
