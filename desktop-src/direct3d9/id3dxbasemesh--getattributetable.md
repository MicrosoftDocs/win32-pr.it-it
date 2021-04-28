---
description: 'Metodo ID3DXBaseMesh::GetAttributeTable: recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: Metodo ID3DXBaseMesh::GetAttributeTable (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115449"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>Metodo ID3DXBaseMesh::GetAttributeTable

Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAttribTable* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Puntatore a una matrice [**di strutture D3DXATTRIBUTERANGE,**](d3dxattributerange.md) che rappresenta le voci nella tabella degli attributi della mesh. Specificare **NULL** per recuperare il valore per pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di voci archiviate in pAttribTable o a un valore da riempire con il numero di voci archiviate nella tabella degli attributi per la mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una tabella degli attributi viene creata da [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) e passa D3DXMESHOPT \_ ATTRSORT per il parametro Flags.

Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi. Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un identificatore di attributo specificato durante il disegno del frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
