---
description: Questo metodo consente all'utente di modificare la dichiarazione di mesh senza modificare il layout dei dati del vertex buffer. La chiamata è valida solo se i formati di dichiarazione precedente e nuovo hanno le stesse dimensioni del vertice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: Metodo ID3DXBaseMesh::UpdateSemantics (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a9a628c16e7f4a26db9953298be1adcba2cef364153d4bb2e6b29dbc4d9ef83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607321"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>Metodo ID3DXBaseMesh::UpdateSemantics

Questo metodo consente all'utente di modificare la dichiarazione di mesh senza modificare il layout dei dati del vertex buffer. La chiamata è valida solo se i formati di dichiarazione precedente e nuovo hanno le stesse dimensioni del vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dichiarazione* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato dei vertici della mesh. Il limite superiore di questa matrice di dichiaratori è [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) viene usato per riformattare e modificare il layout dei dati dei vertici. Ad esempio, usarlo per aggiungere spazio per normali, coordinate di trama, colori, pesi e così via che non erano presenti in precedenza.

**ID3DXBaseMesh::UpdateSemantics** è un metodo per aggiornare la dichiarazione del vertice con informazioni semantiche diverse, senza modificare il layout del vertex buffer. Ad esempio, usarlo per rietichettare una coordinata di trama 3D come binormale o tangente o viceversa.

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

 

 
