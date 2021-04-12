---
description: Crea una mesh da una mesh di patch di controllo.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: Funzione D3DXCreatePatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355859"
---
# <a name="d3dxcreatepatchmesh-function"></a>D3DXCreatePatchMesh (funzione)

Crea una mesh da una mesh di patch di controllo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***

Struttura delle informazioni sulla patch. Per ulteriori informazioni, vedere [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> <dt>

*dwNumPatches* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di patch.

</dd> <dt>

*dwNumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici di controllo nella patch.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Non utilizzato. Riservato per un uso successivo.

</dd> <dt>

*pDecl* \[ in\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che descrive il formato del vertice per la mesh restituita.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo che crea la mesh della patch. Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pPatchMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Puntatore all'oggetto [**ID3DXPatchMesh**](id3dxpatchmesh.md) creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo accetta una mesh patch di input e la converte in una rete tassellati. Le mesh di patch utilizzano buffer di indice a 16 bit. Pertanto, gli indici per [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) sono a 16 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXPATCHINFO**](d3dxpatchinfo.md)
</dt> </dl>

 

 
