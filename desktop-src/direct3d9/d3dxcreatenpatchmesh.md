---
description: Crea una mesh a N patch da una mesh a triangolo.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: Funzione D3DXCreateNPatchMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb23022bfa79ba9bc429bc76a5c42892403b783b4ed634e9b7887b74db126b87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241371"
---
# <a name="d3dxcreatenpatchmesh-function"></a>Funzione D3DXCreateNPatchMesh

Crea una mesh a N patch da una mesh a triangolo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMeshSysMem* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh**](id3dxmesh.md) che rappresenta l'oggetto mesh del triangolo.

</dd> <dt>

*pPatchMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXPatchMesh**](id3dxpatchmesh.md) che rappresenta l'oggetto mesh patch creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




