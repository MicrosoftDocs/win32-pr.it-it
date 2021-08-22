---
description: Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la radice di origine è rappresentata da un'approssimazione sferica aricale (SH), usando il campionamento adattivo.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: Metodo ID3DXPRTEngine::ComputeDirectLightingSHAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 991337b31b10c39cccb622c2838bd53bcb25ad534ae8f896b6ec8f4842072de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801281"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>Metodo ID3DXPRTEngine::ComputeDirectLightingSHAdaptive

Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la radice di origine è rappresentata da un'approssimazione sferica aricale (SH), usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi nella mesh per approssimare in modo più accurato il segnale PRT (Precomputed Radiance Transfer).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
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

Puntatore a un [**oggetto ID3DXPRTBuffer di**](id3dxprtbuffer.md) output. Questo buffer deve avere il numero corretto di canali di colore allocati per la simulazione.

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

 

 
