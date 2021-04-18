---
description: Calcolare le IMT per triangolo da dati per Texel. Questa funzione è simile a D3DXComputeIMTFromTexture, ma usa una matrice float per passare i dati e può calcolare valori dimensionali più alti di 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: Funzione D3DXComputeIMTFromPerTexelSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322868"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a>D3DXComputeIMTFromPerTexelSignal (funzione)

Calcolare le IMT per triangolo da dati per Texel. Questa funzione è simile a [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), ma usa una matrice float per passare i dati e può calcolare valori dimensionali più alti di 4.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo di IMT.

</dd> <dt>

*dwTextureIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*pfTexelSignal* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di Texel di input da cui verrà calcolato IMT. La dimensione della matrice è uWidth \* uHeight \* uComponents.

</dd> <dt>

*uWidth* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Larghezza della trama in pixel.

</dd> <dt>

*uHeight* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altezza della trama in pixel.

</dd> <dt>

*uSignalDimension* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di float per componente in ogni elemento della matrice di segnali.

</dd> <dt>

*uComponents* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Il numero di componenti in ogni Texel.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di incapsulamento della trama. Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Puntatore a una funzione di callback per monitorare lo stato di avanzamento del calcolo di IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato. Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita. Questa matrice può essere fornita come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) di D3DX per definire la priorità dell'allocazione dello spazio di trama nella parametrizzazione della trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Uso di UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
