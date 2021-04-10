---
description: Calcola il contributo di illuminazione diretta per gli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione armonica sferica (SH), usando il campionamento adattivo.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'Metodo ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive (D3DX9Mesh. h)'
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
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762376"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>Metodo ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive

Calcola il contributo di illuminazione diretta per gli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione armonica sferica (SH), usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer).

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

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*AdaptiveThresh* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Soglia sul vettore PRT da usare per la suddivisione dei vertici e delle facce mesh. Se è minore di 1e-6F, viene specificato un valore predefinito di 1e-6F.

</dd> <dt>

*MinEdgeLength* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo. Se il metodo determina che il valore è troppo piccolo, viene specificato un valore dipendente dal modello. Se è zero, viene specificato un valore predefinito pari a 4.

</dd> <dt>

*MaxSubdiv* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output. Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
