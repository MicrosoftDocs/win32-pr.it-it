---
description: Crea un oggetto ID3DXTextureGutterHelper da una mesh di input e da dati di trama.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Funzione D3DXCreateTextureGutterHelper (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e62f89911199497abfd905376f272121c6c5a9996ec5685e556453bc378e65e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045139"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>Funzione D3DXCreateTextureGutterHelper

Crea un [**oggetto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) da una mesh di input e da dati di trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza della trama, in pixel.

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altezza della trama, in pixel.

</dd> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.

</dd> <dt>

*GutterSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Numero di texel in base ai quali eseguire l'over-sample della trama e creare l'area di margine. Deve essere almeno 1.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Puntatore a [**un oggetto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Usa [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) per trasformare una scena in nuove coordinate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento di radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
