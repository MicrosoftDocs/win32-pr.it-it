---
description: 'Metodo ID3DXMesh::SetAttributeTable: imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: Metodo ID3DXMesh::SetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e93bc3f077d239fb93ac23898635dfc2fe5157ed5d78c32719fca6980606658c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606941"
---
# <a name="id3dxmeshsetattributetable-method"></a>Metodo ID3DXMesh::SetAttributeTable

Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAttribTable* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Puntatore a una matrice [**di strutture D3DXATTRIBUTERANGE,**](d3dxattributerange.md) che rappresenta le voci nella tabella degli attributi mesh.

</dd> <dt>

*cAttribTableSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di attributi nella tabella degli attributi mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Se un'applicazione tiene traccia delle informazioni in una tabella di attributi e riorganizza la tabella in seguito a modifiche agli attributi o ai visi, questo metodo consente all'applicazione di aggiornare le tabelle degli attributi anziché chiamare nuovamente [**ID3DXMesh::Optimize.**](id3dxmesh--optimize.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh::LockAttributeBuffer**
</dt> </dl>

 

 
