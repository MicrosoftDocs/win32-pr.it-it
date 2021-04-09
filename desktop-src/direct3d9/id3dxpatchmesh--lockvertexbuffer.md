---
description: Blocca il buffer dei vertici.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'Metodo ID3DXPatchMesh:: LockVertexBuffer (D3DX9Mesh. h)'
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
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886303"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a>Metodo ID3DXPatchMesh:: LockVertexBuffer

Blocca il buffer dei vertici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire. Per questo metodo, i flag validi sono:

-   Eliminazione di D3DLOCK \_
-   D3DLOCK \_ nessun \_ \_ aggiornamento Dirty
-   \_NOSYSLOCK D3DLOCK
-   D3DLOCK \_ ReadOnly
-   Nosovrascrive D3DLOCK \_

Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Puntatore void a un buffer di memoria contenente i dati dei vertici restituiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Il buffer vertex viene in genere bloccato, scritto e quindi sbloccato per la lettura.

Le mesh di patch utilizzano buffer di indice a 16 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
