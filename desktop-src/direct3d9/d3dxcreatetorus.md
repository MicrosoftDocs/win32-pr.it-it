---
description: Usa un sistema di coordinate mancino per creare una mesh contenente un torus.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Funzione D3DXCreateTorus (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1671641a5088535777cb78bf3773f4c1e56e1c3d35e70d345a39df2dad7bd83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526193"
---
# <a name="d3dxcreatetorus-function"></a>Funzione D3DXCreateTorus

Usa un sistema di coordinate mancino per creare una mesh contenente un torus.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla mesh torus creata.

</dd> <dt>

*InnerRadius* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raggio interno del torus. Il valore deve essere maggiore o uguale a 0,0f.

</dd> <dt>

*OuterRadius* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raggio esterno del torus. Il valore deve essere maggiore o uguale a 0,0f.

</dd> <dt>

*Lati* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di lati in una sezione incrociata. Il valore deve essere maggiore o uguale a 3.

</dd> <dt>

*Anelli* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di anelli che fanno parte del torus. Il valore deve essere maggiore o uguale a 3.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore alla forma di output, [**un'interfaccia ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando il metodo viene restituito, questo parametro viene riempito con una matrice di tre DWORD per ogni viso che specificano i tre elementi adiacenti per ogni viso nella mesh. È possibile specificare **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Il torus creato è centrato in corrispondenza dell'origine e il relativo asse è allineato all'asse z. Il raggio interno del torus è il raggio della sezione incrociata (il raggio secondario) e il raggio esterno del torus è il raggio del foro centrale.

Questa funzione restituisce una mesh che può essere usata in un secondo momento per il disegno o la manipolazione da parte dell'applicazione.

Questa funzione crea una mesh con l'opzione di creazione gestita D3DXMESH e \_ [D3DFVF \_ XYZ \| D3DFVF \_ NORMAL](d3dfvf.md) flexible vertex format (FVF).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di disegno delle forme](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
