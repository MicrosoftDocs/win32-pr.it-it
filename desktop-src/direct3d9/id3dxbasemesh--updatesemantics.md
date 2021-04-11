---
description: Questo metodo consente all'utente di modificare la dichiarazione mesh senza modificare il layout dei dati del buffer del vertice. La chiamata è valida solo se il vecchio e il nuovo formato di dichiarazione hanno le stesse dimensioni del vertice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'Metodo ID3DXBaseMesh:: UpdateSemantics (D3DX9Mesh. h)'
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
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058621"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>Metodo ID3DXBaseMesh:: UpdateSemantics

Questo metodo consente all'utente di modificare la dichiarazione mesh senza modificare il layout dei dati del buffer del vertice. La chiamata è valida solo se il vecchio e il nuovo formato di dichiarazione hanno le stesse dimensioni del vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dichiarazione* \[ di in uscita\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che descrive il formato del vertice dei vertici della mesh. Il limite superiore della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

[**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) viene usato per riformattare e modificare il layout dei dati del vertice. Ad esempio, usarlo per aggiungere spazio per normali, coordinate di trama, colori, pesi e così via, che non erano presenti prima.

**ID3DXBaseMesh:: UpdateSemantics** è un metodo per l'aggiornamento della dichiarazione di vertice con informazioni semantiche diverse, senza modificare il layout del buffer dei vertici. Ad esempio, usarlo per rietichettare una coordinata di trama 3D come binormale o tangente oppure viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
