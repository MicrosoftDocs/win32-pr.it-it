---
description: Calcola gli IMT per triangolo da una trama mappata a una mesh, da usare facoltativamente come input per le funzioni UVAtlas D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Funzione D3DXComputeIMTFromTexture (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c0fb2de39cfcc8b0571b05c85ffa3d03945f6c837ae10ba68252b5b9c24b524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299374"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>Funzione D3DXComputeIMTFromTexture

Calcola gli IMT per triangolo da una trama mappata a una mesh, da usare facoltativamente come input per le funzioni [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)D3DX.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'IMT.

</dd> <dt>

*pTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore alla trama (vedere [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) mappata alla mesh.

</dd> <dt>

*dwTextureIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di ritorno a capo automatico della trama. Si tratta di una combinazione di uno o più [**FLAG D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Puntatore a una funzione di callback per monitorare lo stato del calcolo IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato. Utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.

</dd> <dt>

*ppIMTData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita. Questa matrice può essere fornita come input per le funzioni [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) D3DX per classificare in ordine di priorità l'allocazione dello spazio della trama nella parametrizzazione della trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D OK; in caso contrario, il valore \_ è D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Data una trama mappata sulla superficie della mesh, l'algoritmo calcola l'IMT per ogni viso. In questo modo, i triangoli contenenti dati dei segnali a frequenza più bassa avranno meno spazio nell'at atlas finale della trama se parametrizzati con le funzioni UVAtlas. Si presuppone che la trama sia interpolata in modo bilineare sulla mesh.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Uso di UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
