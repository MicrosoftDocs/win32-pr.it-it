---
description: Moltiplica ogni vettore PRT (Precomputed Radiance Transfer) per l'albedo per vertice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: Metodo ID3DXPRTEngine::MultiplyAlbedo (D3DX9Mesh.h)
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
ms.openlocfilehash: c2989ce2a662be5a1ec53c961b8fafa072862fc2b43b6003b04f6b887ef3c077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790541"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>Metodo ID3DXPRTEngine::MultiplyAlbedo

Moltiplica ogni vettore PRT (Precomputed Radiance Transfer) per l'albedo per vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che conterrà vettori PRT moltiplicati per l'albedo per vertice. Se questo buffer di output è un oggetto trama, è necessario fare attenzione a archiviare l'albedo della trama alla stessa risoluzione del buffer di simulazione. È possibile impostare la risoluzione appropriata nell'albedo [**con D3DXLoadSurfaceFromSurface,**](d3dxloadsurfacefromsurface.md)applicando le aree di navigazione trame, se appropriato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

I metodi ID3DXPRTEngine::Computexxx calcolano i buffer di output in cui il segnale di luce non è stato moltiplicato per albedo. Non moltiplicando l'albedo, è possibile modellare la variazione di albedo su una scala più fine rispetto alla luminosità di origine, producendo risultati più accurati dalla compressione.

Per includere albedo nel modello con luce di rendering, chiamare questo metodo dopo uno dei metodi Computexxx.

[**È necessario chiamare ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




