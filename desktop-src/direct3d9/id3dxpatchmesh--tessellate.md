---
description: Esegue un'operazione a più livelli uniforme in base al livello a più livelli.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: Metodo ID3DXPatchMesh::Tessellate (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bd1bb3f242078603f84a0ff12c05c0e824a55e759f147c8aa230490ab36af39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802011"
---
# <a name="id3dxpatchmeshtessellate-method"></a>Metodo ID3DXPatchMesh::Tessellate

Esegue un'operazione a più livelli uniforme in base al livello a più livelli.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTessLevel* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Livello a tessellazione. Questo è il numero di vertici introdotti tra i vertici esistenti. L'intervallo di questo parametro float è 0 < fTessLevel <= 32.

</dd> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh a trama risultante. Vedere [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione funzionerà in modo più efficiente se la mesh di patch è stata ottimizzata usando [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
