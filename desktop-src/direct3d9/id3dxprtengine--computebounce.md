---
description: Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso. Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello PRT (precomputed Radiance Transfer) basato su SH (sferica).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'Metodo ID3DXPRTEngine:: ComputeBounce (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355704"
---
# <a name="id3dxprtenginecomputebounce-method"></a>Metodo ID3DXPRTEngine:: ComputeBounce

Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso. Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello PRT (precomputed Radiance Transfer) basato su SH (sferica).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
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

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella un singolo rimbalzo della luce con riflesso. Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.

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

Usare la sequenza chiamante seguente per modellare più rimbalzi luce con illuminazione diretta.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



Usare la sequenza chiamante seguente per modellare più rimbalzi luce con la dispersione della superficie.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



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

[**ID3DXPRTEngine::ComputeSS**](id3dxprtengine--computess.md)
</dt> </dl>

 

 




