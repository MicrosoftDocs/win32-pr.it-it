---
description: Moltiplica ogni vettore PRT (pre-Computed Radiance Transfer) per l'albedo per vertice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'Metodo ID3DXPRTEngine:: MultiplyAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323439"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>Metodo ID3DXPRTEngine:: MultiplyAlbedo

Moltiplica ogni vettore PRT (pre-Computed Radiance Transfer) per l'albedo per vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che conterrà vettori PRT moltiplicato per l'albedo per vertice. Se il buffer di output è un oggetto trama, è necessario prestare attenzione per archiviare l'albedo della trama con la stessa risoluzione del buffer di simulazione. È possibile impostare la risoluzione corretta nell'albedo con [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applicando le aree di rilegatura delle trame, se necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

I metodi ID3DXPRTEngine:: Computexxx calcolano i buffer di output in cui il segnale chiaro non è stato moltiplicato per albedo. Se non si moltiplica l'albedo, è possibile modellare la variazione dell'albedo a una scala più sottile rispetto alla luminosità di origine, ottenendo così risultati più accurati dalla compressione.

Per includere albedo nel modello Light con rendering, chiamare questo metodo dopo uno dei metodi Computexxx.

[**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) deve essere chiamato prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




