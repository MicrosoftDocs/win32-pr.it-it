---
description: Aggiorna le informazioni sull'influenza ossea in modo che corrispondano ai vertici dopo essere stati riordinati. Questo metodo deve essere chiamato se il buffer dei vertici di destinazione è stato riordinato esternamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'Metodo ID3DXSkinInfo:: mapping (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322059"
---
# <a name="id3dxskininforemap-method"></a>Metodo ID3DXSkinInfo:: mapping

Aggiorna le informazioni sull'influenza ossea in modo che corrispondano ai vertici dopo essere stati riordinati. Questo metodo deve essere chiamato se il buffer dei vertici di destinazione è stato riordinato esternamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici di cui modificare il mapping.

</dd> <dt>

*pVertexRemap* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD la cui lunghezza è specificata da NumVertices.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Ogni elemento in pVertexRemap specifica l'indice Vertex precedente per tale posizione. Se, ad esempio, un vertice si trova nella posizione 3 ma è stato rimappato alla posizione 5, il quinto elemento di pVertexRemap deve contenere 3. È possibile usare la matrice di riassociazione dei vertici restituita da [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
