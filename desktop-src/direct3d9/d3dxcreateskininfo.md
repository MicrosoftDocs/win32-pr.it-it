---
description: 'Funzione D3DXCreateSkinInfo: crea un oggetto mesh di interfaccia vuoto usando un dichiaratore.'
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Funzione D3DXCreateSkinInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da582d791b27d30c78583972e6f598af8af3eb9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102739"
---
# <a name="d3dxcreateskininfo-function"></a>Funzione D3DXCreateSkinInfo

Crea un oggetto mesh dell'interfaccia vuota usando un dichiaratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumVertices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici per la mesh dell'interfaccia.

</dd> <dt>

*pDeclaration* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice per la mesh restituita.

</dd> <dt>

*NumBones* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di elementi per la mesh dell'interfaccia.

</dd> <dt>

*ppSkinInfo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXSkinInfo,**](id3dxskininfo.md) che rappresenta l'oggetto mesh dell'interfaccia creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Usare [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) per popolare l'oggetto mesh dell'interfaccia vuota restituito da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
