---
description: Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: 'Metodo ID3DXMesh:: SetAttributeTable (D3DX9Mesh. h)'
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
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322323"
---
# <a name="id3dxmeshsetattributetable-method"></a>Metodo ID3DXMesh:: SetAttributeTable

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

*pAttribTable* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Puntatore a una matrice di strutture [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , che rappresenta le voci nella tabella dell'attributo mesh.

</dd> <dt>

*cAttribTableSize* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di attributi nella tabella dell'attributo mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Se un'applicazione tiene traccia delle informazioni in una tabella degli attributi e riorganizza la tabella in seguito a modifiche apportate agli attributi o ai visi, questo metodo consente all'applicazione di aggiornare le tabelle degli attributi anziché chiamare di nuovo [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh:: LockAttributeBuffer**
</dt> </dl>

 

 
