---
description: Calcola la luminosità di origine risultante da un singolo rimbalzo di luce interreflected, usando il campionamento adattivo.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: Metodo ID3DXPRTEngine::ComputeBounceAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: efe983a0160d46910e7b8d1e29d0042d801275ef70aef30f6050e0538b6f9927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729750"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>Metodo ID3DXPRTEngine::ComputeBounceAdaptive

Calcola la luminosità di origine risultante da un singolo rimbalzo di luce interreflected, usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi nella mesh per approssimare in modo più accurato il segnale PRT (Precomputed Radiance Transfer). Questo metodo può essere usato per qualsiasi scena accesa, incluso un modello PRT sferico basato su sh(SH).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer di**](id3dxprtbuffer.md) input che rappresenta l'oggetto 3D del precedente bounce di luce. Questo buffer di input deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> <dt>

*AdaptiveThresh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Soglia sul vettore PRT da usare per la suddivisione di vertici e visi della mesh. Se è minore di 1e-6f, viene specificato il valore predefinito 1e-6f.

</dd> <dt>

*MinEdgeLength* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Lunghezza minima del bordo del viso che verrà generata nel campionamento adattivo. Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello. Se zero, viene specificato il valore predefinito 4.

</dd> <dt>

*MaxSubdiv* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Livello massimo di suddivisione di un viso che verrà usato nel campionamento adattivo.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer di**](id3dxprtbuffer.md) output. Questo buffer di output deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che mantiene una somma in esecuzione di pDataOut con ogni calcolo di light bounce. Può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
