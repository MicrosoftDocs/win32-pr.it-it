---
description: Crea un oggetto ID3DXTextureGutterHelper da una mesh di input e dati di trama.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Funzione D3DXCreateTextureGutterHelper (D3DX9Mesh. h)
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
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322723"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>D3DXCreateTextureGutterHelper (funzione)

Crea un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) da una mesh di input e dati di trama.

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

*Larghezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Larghezza, in pixel, della trama.

</dd> <dt>

*Altezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altezza, in pixel, della trama.

</dd> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.

</dd> <dt>

*GutterSize* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Numero di Texel in base ai quali sovracampionare la trama e creare l'area di gronda. Deve essere almeno 1.

</dd> <dt>

*ppBuffer* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Puntatore a un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Usare [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) per trasformare una scena in nuove coordinate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
