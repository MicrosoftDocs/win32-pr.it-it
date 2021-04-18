---
description: Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso, usando il campionamento adattivo.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'Metodo ID3DXPRTEngine:: ComputeBounceAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323454"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>Metodo ID3DXPRTEngine:: ComputeBounceAdaptive

Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso, usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer). Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello di PRT a sferica (SH).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeBounceAdaptive(
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

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output. Questo buffer di output deve avere il numero appropriato di canali di colore allocati per la simulazione.

</dd> <dt>

*pDataTotal* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che mantiene una somma in esecuzione di pDataOut con ogni calcolo di rimbalzo chiaro. Può essere **null**.

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

 

 
