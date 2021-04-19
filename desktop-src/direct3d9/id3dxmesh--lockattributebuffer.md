---
description: Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'Metodo ID3DXMesh:: LockAttributeBuffer (D3DX9Mesh. h)'
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
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322324"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>Metodo ID3DXMesh:: LockAttributeBuffer

Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di zero o più flag di blocco che descrivono il tipo di blocco da eseguire. Per questo metodo, i flag validi sono:

-   Eliminazione di D3DLOCK \_
-   D3DLOCK \_ nessun \_ \_ aggiornamento Dirty
-   \_NOSYSLOCK D3DLOCK
-   D3DLOCK \_ ReadOnly

Per una descrizione dei flag, vedere [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Indirizzo di un puntatore a un buffer contenente un valore DWORD per ogni viso della mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Se è stato chiamato [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) , per la mesh sarà disponibile anche una tabella di attributi a cui è possibile accedere tramite il metodo [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh:: SetAttributeTable**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
