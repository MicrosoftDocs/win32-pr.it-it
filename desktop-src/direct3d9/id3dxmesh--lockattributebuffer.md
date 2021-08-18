---
description: Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore a esso.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: Metodo ID3DXMesh::LockAttributeBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ca767c6bc223c40d6013b93162de057aac9f4fb1b71303990f9128e4eca1ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802154"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>Metodo ID3DXMesh::LockAttributeBuffer

Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore a esso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire. Per questo metodo, i flag validi sono:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ NO \_ DIRTY \_ UPDATE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY

Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Indirizzo di un puntatore a un buffer contenente un valore DWORD per ogni viso nella mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Se è stato chiamato [**ID3DXMesh::Optimize,**](id3dxmesh--optimize.md) la mesh avrà anche una tabella di attributi accessibile tramite il metodo [**ID3DXBaseMesh::GetAttributeTable.**](id3dxbasemesh--getattributetable.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh::SetAttributeTable**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
