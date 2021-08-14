---
description: Clona una mesh usando un dichiaratore.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: Metodo ID3DXBaseMesh::CloneMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fec8b0881cdef43051afcb06d63ec20284cb116299912ce0acf7ac4c54a0f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521864"
---
# <a name="id3dxbasemeshclonemesh-method"></a>Metodo ID3DXBaseMesh::CloneMesh

Clona una mesh usando un dichiaratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [**flag D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.

</dd> <dt>

*pDeclaration* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che specificano il formato dei vertici per i vertici nella mesh di output.

</dd> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh clonata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

**ID3DXBaseMesh::CloneMesh** viene usato per riformattare e modificare il layout dei dati dei vertici. Questa operazione viene eseguita creando un nuovo oggetto mesh. Ad esempio, usarlo per aggiungere spazio per normali, coordinate della trama, colori, pesi e così via che non erano presenti in precedenza.

[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) aggiorna la dichiarazione dei vertici con informazioni semantiche diverse senza modificare il layout del vertex buffer. Questo metodo non modifica il contenuto del vertex buffer. Ad esempio, usarlo per rietichettare una coordinata di trama 3D come binormale o tangente o viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
