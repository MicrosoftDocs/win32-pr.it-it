---
description: Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH). Il calcolo dell'illuminazione sulla GPU sarà in genere molto più veloce rispetto alla CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'Metodo ID3DXPRTEngine:: ComputeDirectLightingSHGPU (D3DX9Mesh. h)'
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
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323685"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>Metodo ID3DXPRTEngine:: ComputeDirectLightingSHGPU

Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH). Il calcolo dell'illuminazione sulla GPU sarà in genere molto più veloce rispetto alla CPU.

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

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore all'oggetto dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato per eseguire la simulazione sulla GPU. Il dispositivo deve supportare i pixel shader [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) .

> [!Note]  
> Le funzioni di callback non devono usare l'oggetto dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usato dal simulatore della GPU.

 

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Parametro di simulazione GPU che definisce la risoluzione del buffer z dell'ombreggiatura. Deve essere impostato su uno dei valori costanti di [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md). Per specificare una simulazione di precisione più elevata, il \_ valore Highquality di D3DXSHGPUSIMOPT può essere combinato con uno dei \_ valori SHADOWRESXXX di D3DXSHGPUSIMOPT.

</dd> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*ZBias* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distorsione nella direzione normale.

</dd> <dt>

*ZAngleBias* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distorsione nella direzione normale, ridimensionata di uno meno il coseno dell'angolo con il raggio chiaro.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

In questo metodo, l'albedo non viene moltiplicato per il segnale chiaro e solo la luce in ingresso è integrata nel simulatore. Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.

Chiamare [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore di traslazione di radiazione (PRT) pre-calcolato per l'albedo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
