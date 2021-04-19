---
description: 'Calcola un vettore di trasferimento che esegue il mapping della luminosità di origine alla luminosità di uscita risultante dalla dispersione della sottosuperficie, usando il campionamento adattivo e le proprietà del materiale impostate da ID3DXPRTEngine:: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'Metodo ID3DXPRTEngine:: ComputeSSAdaptive (D3DX9Mesh. h)'
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
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323683"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>Metodo ID3DXPRTEngine:: ComputeSSAdaptive

Calcola un vettore di trasferimento che esegue il mapping della luminosità di origine alla luminosità di uscita risultante dalla dispersione della sottosuperficie, usando il campionamento adattivo e le proprietà del materiale impostate da [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Il metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer). Questo metodo può essere utilizzato solo per i materiali definiti per ogni vertice in un oggetto mesh.

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

*pDataIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente. Questo buffer di input deve avere il numero appropriato di canali di colore allocati per la simulazione.

</dd> <dt>

*AdaptiveThresh* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Soglia sul vettore PRT da usare per la suddivisione dei vertici e delle facce mesh. Se è minore di 1e-6F, viene specificato un valore predefinito di 1e-6F.

</dd> <dt>

*MinEdgeLength* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo. Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello.

</dd> <dt>

*MaxSubdiv* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo. Se è zero, viene specificato un valore predefinito pari a 4.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella un singolo rimbalzo della sottosuperficie. Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.

</dd> <dt>

*pDataTotal* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che corrisponde alla somma in corso di tutti gli output pDataOut precedenti. Può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Per modellare la dispersione della sottosuperficie, chiamare questo metodo per ogni rimbalzo chiaro dopo la chiamata di un metodo [**ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) .

L'output di questo metodo non include l'albedo e solo la luce in ingresso è integrata nel simulatore. Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.

Chiamare [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore PRT per l'albedo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
