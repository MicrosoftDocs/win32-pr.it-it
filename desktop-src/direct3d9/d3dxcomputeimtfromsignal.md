---
description: Calcola gli IMT per triangolo da un segnale personalizzato specificato dall'applicazione che varia sulla superficie della mesh (in genere con una frequenza superiore rispetto ai dati dei vertici). Il segnale viene valutato tramite una funzione di callback specificata dall'utente.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Funzione D3DXComputeIMTFromSignal (D3DX9Mesh.h)
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
ms.openlocfilehash: 9d645e12f7159963f9b9bc5abeb960aee0bac2282537c482465be3ea08690181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299413"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>Funzione D3DXComputeIMTFromSignal

Calcola gli IMT per triangolo da un segnale personalizzato specificato dall'applicazione che varia sulla superficie della mesh (in genere con una frequenza superiore rispetto ai dati dei vertici). Il segnale viene valutato tramite una funzione di callback specificata dall'utente.

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

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'IMT.

</dd> <dt>

*dwTextureIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*uSignalDimension* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di componenti in ogni punto dati nel segnale.

</dd> <dt>

*fMaxUVDistance* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distanza massima tra i vertici. L'algoritmo continua a essere suddiviso fino a quando la distanza tra tutti i vertici è minore o uguale a fMaxUVDistance.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di ritorno a capo automatico della trama. Si tratta di una combinazione di uno o più [**FLAG D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pSignalCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Puntatore a una funzione dell'analizzatore fornita dall'utente, che verrà usata per calcolare il valore del segnale in corrispondenza di coordinate U,V arbitrarie. La funzione segue il prototipo [di LPD3DXIMTSIGNALCALLBACK.](lpd3dximtsignalcallback.md)

</dd> <dt>

*pUserData* \[ Pollici\]
</dt> <dd>

Tipo: **\* VOID**

Puntatore a un valore definito dall'utente passato alla funzione di callback del segnale. Utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.

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

Questa funzione richiede che la mesh di input contenga un mapping di trama da segnale a mesh (ad esempio coordinate di trama). Consente all'utente di definire un segnale in modo arbitrario sulla superficie della mesh.

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

 

 
