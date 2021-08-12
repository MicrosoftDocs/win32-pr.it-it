---
description: Calcola la luminosità di origine risultante dalla dispersione sottosurface, usando le proprietà dei materiali impostate da ID3DXPRTEngine::SetMeshMaterials. Questo metodo può essere usato solo per i materiali definiti per vertice in un oggetto mesh.
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: Metodo ID3DXPRTEngine::ComputeSS (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b34561bf96983506cbb0f484f273de9a5e0f0b6138db2e1ddbb92b19c8bcd18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294021"
---
# <a name="id3dxprtenginecomputess-method"></a>Metodo ID3DXPRTEngine::ComputeSS

Calcola la luminosità di origine risultante dalla dispersione dei subsurface, usando le proprietà dei materiali impostate da [**ID3DXPRTEngine::SetMeshMaterials.**](id3dxprtengine--setmeshmaterials.md) Questo metodo può essere usato solo per i materiali definiti per vertice in un oggetto mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
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

Per modellare la dispersione dei sottoprogetti, chiamare questo metodo per ogni leggero rimbalzo dopo la chiamata di un metodo ID3DXPRTEngine::ComputeDirectLighting.

Usare la sequenza di chiamata seguente per modellare la dispersione sotto la superficie.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



L'output di questo metodo non include albedo e solo la luce in ingresso è integrata nel simulatore. Non moltiplicando l'albedo, è possibile modellare la variazione di albedo su una scala più fine rispetto alla radice di origine, producendo risultati più accurati dalla compressione.

Chiamare [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore PRT (Precomputed Radiance Transfer) per albedo.

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
</dt> </dl>

 

 




