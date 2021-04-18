---
description: Calcola gli IMT per triangolo da un segnale personalizzato specificato dall'applicazione che varia in base alla superficie della mesh, in genere con una frequenza maggiore rispetto ai dati dei vertici. Il segnale viene valutato tramite una funzione di callback specificata dall'utente.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Funzione D3DXComputeIMTFromSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323033"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>D3DXComputeIMTFromSignal (funzione)

Calcola gli IMT per triangolo da un segnale personalizzato specificato dall'applicazione che varia in base alla superficie della mesh, in genere con una frequenza maggiore rispetto ai dati dei vertici. Il segnale viene valutato tramite una funzione di callback specificata dall'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
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

*uSignalDimension* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di componenti in ogni punto dati del segnale.

</dd> <dt>

*fMaxUVDistance* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distanza massima tra i vertici; l'algoritmo continua la suddivisione fino a quando la distanza tra tutti i vertici è minore o uguale a fMaxUVDistance.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di incapsulamento della trama. Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pSignalCallback* \[ in\]
</dt> <dd>

Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore del segnale a coordinate U, V arbitrarie. La funzione segue il prototipo di [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).

</dd> <dt>

*pUserData* \[ in\]
</dt> <dd>

Tipo: **void \***

Puntatore a un valore definito dall'utente che viene passato alla funzione di callback del segnale. Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

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

## <a name="remarks"></a>Commenti

Questa funzione richiede che la mesh di input contenga un mapping di trama da segnale a mesh, ad esempio coordinate di trama. Consente all'utente di definire un segnale arbitrariamente sulla superficie della mesh.

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

 

 
