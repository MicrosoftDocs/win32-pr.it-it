---
description: Aggiorna le informazioni sull'influenza dell'osso in modo che corrispondano ai vertici dopo che sono stati riordinati. Questo metodo deve essere chiamato se il vertex buffer di destinazione è stato riordinato esternamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: Metodo ID3DXSkinInfo::Remap (D3DX9Mesh.h)
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
ms.openlocfilehash: 941a71539184b7d49e35627c932da77b4494486c35506b1b4e5f69ad52c40829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727781"
---
# <a name="id3dxskininforemap-method"></a>Metodo ID3DXSkinInfo::Remap

Aggiorna le informazioni sull'influenza dell'osso in modo che corrispondano ai vertici dopo che sono stati riordinati. Questo metodo deve essere chiamato se il vertex buffer di destinazione è stato riordinato esternamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumVertices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici di cui eseguire il nuovo mapping.

</dd> <dt>

*pVertexRemap* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORDS la cui lunghezza è specificata da NumVertices.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Ogni elemento in pVertexRemap specifica l'indice dei vertici precedente per tale posizione. Ad esempio, se un vertice si è posizionato nella posizione 3 ma è stato mappato nuovamente alla posizione 5, il quinto elemento di pVertexRemap deve contenere 3. È possibile usare la matrice di mapping dei vertici restituita da [**ID3DXMesh::Optimize.**](id3dxmesh--optimize.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
