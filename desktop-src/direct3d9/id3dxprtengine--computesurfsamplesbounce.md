---
description: Calcola gli esempi di trasferimento di raggi pre-calcolati (PRT) per un punto arbitrario (e un vettore normale).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: Metodo ID3DXPRTEngine::ComputeSurfSamplesBounce (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 925b5da620ae665e0fa863527c196b65a5dfcb17dd81de1c25a23b907cb88ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492711"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a>Metodo ID3DXPRTEngine::ComputeSurfSamplesBounce

Calcola gli esempi di trasferimento di raggi pre-calcolati (PRT) per un punto arbitrario (e un vettore normale).

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSurfDataIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta la luminosità di origine dell'oggetto 3D. Questo buffer di input deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> <dt>

*NumSamples* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di posizioni di esempio.

</dd> <dt>

*pSampleLocs* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posizione per ogni campione.

</dd> <dt>

*pSampleNorms* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Vettore normale per ogni posizione del campione.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che modella il contributo di illuminazione diretta al punto, usando l'approssimazione armonica sferica (SH).

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) facoltativo che rappresenta la somma in esecuzione di tutti gli output pDataOut precedenti. Può essere **NULL.**

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

[**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
