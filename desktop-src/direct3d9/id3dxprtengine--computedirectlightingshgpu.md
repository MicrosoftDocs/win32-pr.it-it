---
description: Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione sferica arica (SH). Il calcolo dell'illuminazione della GPU sarà in genere molto più veloce rispetto alla CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: Metodo ID3DXPRTEngine::ComputeDirectLightingSHGPU (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14dc76cb8ac3875101c42beb581c7eb2b96eb7511c85e7f76cd034658afcca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985581"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>Metodo ID3DXPRTEngine::ComputeDirectLightingSHGPU

Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione sferica arica (SH). Il calcolo dell'illuminazione della GPU sarà in genere molto più veloce rispetto alla CPU.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore [**all'oggetto dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per eseguire la simulazione nella GPU. Il dispositivo deve supportare ps 2 pixel shader da [ \_ \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel.

> [!Note]  
> Le funzioni di callback non devono usare [**l'oggetto dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato dal simulatore GPU.

 

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Parametro di simulazione GPU che definisce la risoluzione dell'ombreggiatura z-buffer. Deve essere impostato su uno dei valori costanti di [**D3DXSHGPUSIMOPT.**](./d3dxshgpusimopt.md) Per specificare una simulazione di precisione più elevata, il valore D3DXSHGPUSIMOPT HIGHQUALITY può essere combinato con uno dei valori \_ D3DXSHGPUSIMOPT \_ SHADOWRESxxx.

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*ZBias* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distorsione nella direzione normale.

</dd> <dt>

*ZAngleBias* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distorsione in direzione normale, ridimensionata di uno meno il coseno dell'angolo con il raggio di luce.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a [**un oggetto ID3DXPRTBuffer.**](id3dxprtbuffer.md) Questo buffer deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

In questo metodo, l'albedo non viene moltiplicato per il segnale di luce e solo la luce in ingresso è integrata nel simulatore. Non moltiplicando l'albedo, è possibile modellare la variazione di albedo su una scala più fine rispetto alla radice di origine, producendo risultati più accurati dalla compressione.

Chiamare [**MultiplyAlbedo per**](id3dxprtengine--multiplyalbedo.md) moltiplicare ogni vettore PRT (Precomputed Radiance Transfer) per l'albedo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
