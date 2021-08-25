---
description: Calcola un vettore di trasferimento che esegue il mapping della radice di origine per uscire dalla dispersione delle sottoaree, usando il campionamento adattivo e le proprietà dei materiali impostate da ID3DXPRTEngine::SetMeshMaterials.
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: Metodo ID3DXPRTEngine::ComputeSSAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a602566c4d0e5b3cb5c68b2f983b6c56a9d9f596ee673db97a72e6054837759b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847381"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>Metodo ID3DXPRTEngine::ComputeSSAdaptive

Calcola un vettore di trasferimento che esegue il mapping della radice di origine per uscire dalla dispersione delle sottoaree, usando il campionamento adattivo e le proprietà materiali impostate da [**ID3DXPRTEngine::SetMeshMaterials.**](id3dxprtengine--setmeshmaterials.md) Il metodo genera nuovi vertici e visi nella mesh per approssimare in modo più accurato il segnale PRT (Precomputed Radiance Transfer). Questo metodo può essere usato solo per i materiali definiti per vertice in un oggetto mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeSSAdaptive(
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

Lunghezza minima del bordo del viso che verrà generata nel campionamento adattivo. Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello.

</dd> <dt>

*MaxSubdiv* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Livello massimo di suddivisione di un viso che verrà usato nel campionamento adattivo. Se zero, viene specificato il valore predefinito 4.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella un singolo butto della luce sparse sotto la superficie. Questo buffer di output deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che rappresenta la somma corrente di tutti gli output pDataOut precedenti. Può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Per modellare la dispersione delle sottoaree, chiamare questo metodo per ogni luce che si riaccetta dopo la chiamata di un metodo [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive.**](id3dxprtengine--computedirectlightingshadaptive.md)

L'output di questo metodo non include albedo e solo la luce in ingresso è integrata nel simulatore. Non moltiplicando l'albedo, è possibile modellare la variazione di albedo su una scala più fine rispetto alla radice di origine, producendo risultati più accurati dalla compressione.

Chiamare [**ID3DXPRTEngine::MultiplyAlbedo per**](id3dxprtengine--multiplyalbedo.md) moltiplicare ogni vettore PRT per l'albedo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
