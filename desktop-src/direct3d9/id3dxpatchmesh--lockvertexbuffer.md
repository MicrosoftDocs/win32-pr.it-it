---
description: Bloccare il buffer dei vertici.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: Metodo ID3DXPatchMesh::LockVertexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae385d636429d25b420f1bc75dd531b55d8d2419a7eedc328865753d7b7b536b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120735"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a>Metodo ID3DXPatchMesh::LockVertexBuffer

Bloccare il buffer dei vertici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire. Per questo metodo, i flag validi sono:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ NO \_ DIRTY \_ UPDATE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE

Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Puntatore \* VOID a un buffer di memoria contenente i dati dei vertici restituiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Il buffer dei vertici viene in genere bloccato, scritto e quindi sbloccato per la lettura.

Le mesh di patch usano buffer di indice a 16 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
