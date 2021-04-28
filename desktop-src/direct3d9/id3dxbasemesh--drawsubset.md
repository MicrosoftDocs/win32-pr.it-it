---
description: 'Metodo ID3DXBaseMesh::D rawSubset: disegna un subset di una mesh.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: Metodo ID3DXBaseMesh::D rawSubset (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115469"
---
# <a name="id3dxbasemeshdrawsubset-method"></a>Metodo ID3DXBaseMesh::D rawSubset

Disegna un subset di una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AttribId* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Valore DWORD che specifica il subset della mesh da disegnare. Questo valore viene usato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Il subset specificato da AttribId verrà sottoposto a rendering dal metodo [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) usando il tipo primitivo D3DPT TRIANGLELIST, quindi un index buffer deve essere inizializzato \_ correttamente.

Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi. Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un identificatore di attributo specificato (*AttribId*) durante il disegno del frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
