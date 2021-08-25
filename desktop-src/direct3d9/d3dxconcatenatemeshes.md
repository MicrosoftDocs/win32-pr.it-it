---
description: Concatena un gruppo di mesh in un'unica mesh comune. Questo metodo può facoltativamente applicare una trasformazione matrice a ogni mesh di input e alle relative coordinate di trama.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Funzione D3DXConcatenateMeshes (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21801c2f4b8ef8dd2a34c9788b402128da4ce4fed33c3c38a08e61c35a847e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857391"
---
# <a name="d3dxconcatenatemeshes-function"></a>Funzione D3DXConcatenateMeshes

Concatena un gruppo di mesh in un'unica mesh comune. Questo metodo può facoltativamente applicare una trasformazione matrice a ogni mesh di input e alle relative coordinate di trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMeshes* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Matrice di puntatori della mesh di input (vedere [**ID3DXMesh).**](id3dxmesh.md) Il numero di elementi nella matrice è NumMeshes.

</dd> <dt>

*NumMeshes* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di mesh di input da concatenare.

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di creazione della mesh; si tratta di una combinazione di uno o [**più flag D3DXMESH.**](./d3dxmesh.md) Le opzioni di creazione della mesh sono equivalenti al parametro options richiesto da [**D3DXCreateMesh.**](d3dxcreatemesh.md)

</dd> <dt>

*pGeomXForms* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice facoltativa di trasformazioni geometriche. Il numero di elementi nella matrice è NumMeshes; ogni elemento è una matrice di trasformazione (vedere [**D3DXMATRIX).**](d3dxmatrix.md) Può essere **NULL.**

</dd> <dt>

*pTextureXForms* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice facoltativa di trasformazioni di trama. Il numero di elementi nella matrice è NumMeshes; ogni elemento è una matrice di trasformazione (vedere [**D3DXMATRIX).**](d3dxmatrix.md) Questo parametro può essere **NULL.**

</dd> <dt>

*pDecl* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntatore facoltativo a una dichiarazione di vertice (vedere [**D3DVERTEXELEMENT9).**](d3dvertexelement9.md) Questo parametro può essere **NULL.**

</dd> <dt>

*pD3DDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per creare la nuova mesh.

</dd> <dt>

*ppMeshOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore alla mesh creata (vedere [**ID3DXMesh).**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Se non [viene](vertex-declaration.md) specificata alcuna dichiarazione di vertice come parte del parametro options mesh creation, il metodo genererà un'unione di tutte le dichiarazioni di vertice delle sottomese, innalzando di livello i canali e i tipi, se necessario. Il metodo creerà una tabella di attributi dalle tabelle degli attributi delle mesh di input. Per garantire la creazione di una tabella di attributi, chiamare [**Optimize**](id3dxmesh--optimize.md) with Flags (Ottimizza con flag) impostato su D3DXMESHOPT COMPACT e \_ D3DXMESHOPT \_ ATTRSORT (vedere [**D3DXMESHOPT).**](./d3dxmeshopt.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
