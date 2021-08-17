---
description: Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la radice di origine è rappresentata da un'approssimazione sferica arica (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: Metodo ID3DXPRTEngine::ComputeDirectLightingSH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51eb3121501cee7c56385a9083fc689cd8a06759443250f64bae16901779a3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729713"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>Metodo ID3DXPRTEngine::ComputeDirectLightingSH

Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la radice di origine è rappresentata da un'approssimazione sferica arica (SH).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella il contributo di illuminazione diretta con l'approssimazione SH. Questo buffer deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'output non include albedo e solo la luce in ingresso è integrata nel simulatore. Non moltiplicando l'albedo, è possibile modellare la variazione di albedo su una scala più fine rispetto alla radice di origine, producendo risultati più accurati dalla compressione.

Chiamare [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) per moltiplicare ogni vettore PRT (Precomputed Radiance Transfer) per albedo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
