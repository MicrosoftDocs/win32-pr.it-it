---
description: Usa un sistema di coordinate mancino per creare una mesh contenente una sfera.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Funzione D3DXCreateSphere (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c1cea000071f0d097f29138b4e5f2db554f2214d8ca6343c16a39740d82c29e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119351"
---
# <a name="d3dxcreatesphere-function"></a>Funzione D3DXCreateSphere

Usa un sistema di coordinate mancino per creare una mesh contenente una sfera.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla mesh sphere creata.

</dd> <dt>

*Raggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raggio della sfera. Questo valore deve essere maggiore o uguale a 0,0f.

</dd> <dt>

*Sezioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di sezioni sull'asse principale.

</dd> <dt>

*Stack* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di stack lungo l'asse principale.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore alla forma di output, [**un'interfaccia ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando il metodo viene restituito, questo parametro viene riempito con una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh. È possibile specificare **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

La sfera creata è centrata sull'origine e il relativo asse è allineato all'asse z.

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

 

 
