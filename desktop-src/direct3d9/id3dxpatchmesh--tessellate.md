---
description: Esegue lo schema a mosaico uniforme in base al livello del mosaico.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'Metodo ID3DXPatchMesh:: conteggiarla suddividerla (D3DX9Mesh. h)'
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
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323714"
---
# <a name="id3dxpatchmeshtessellate-method"></a>Metodo ID3DXPatchMesh:: conteggiarla suddividerla

Esegue lo schema a mosaico uniforme in base al livello del mosaico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTessLevel* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Livello mosaico. Il numero di vertici introdotti tra i vertici esistenti. L'intervallo di questo parametro float è 0 < fTessLevel <= 32.

</dd> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh tassellati risultante. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione verrà eseguita in modo più efficiente se la mesh patch è stata ottimizzata con [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
