---
description: Calcola una proiezione dell'illuminazione diretta dal mancato rilascio della luce precedente in vettori di base sferici aricali (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: Metodo ID3DXPRTEngine::ComputeVolumeSamples (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edc13e8b6f0e5c725e957be22f1b297f825a4f3b622ced68adf19b34a0b64b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293502"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>Metodo ID3DXPRTEngine::ComputeVolumeSamples

Calcola una proiezione dell'illuminazione diretta dal mancato rilascio della luce precedente in vettori di base sferici aricali (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSurfDataIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer di**](id3dxprtbuffer.md) input che rappresenta l'oggetto 3D del precedente bounce di luce.

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*NumVolSamples.xml* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di posizioni di esempio.

</dd> <dt>

*pSampleLocs* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posizione per ogni campione. Se pSampleLocs è **NULL,** ComputeVolumeSamples calcola le matrici di trasferimento a ogni vertice mesh. Tuttavia, se pSampleLocs non è **NULL,** è necessario eseguire il campionamento su una sfera (impostare UseSphere = **TRUE** e UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); In caso contrario, ComputeVolumeSamples restituirà D3DERR \_ INVALIDCALL.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che proietta l'illuminazione diretta dal precedente flusso di luce nei vettori di base SH. Questo buffer deve avere il numero corretto di canali di colore allocati per la simulazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo calcola il modo in cui la luce della funzione di luminosità di origine viene riflessa dalla superficie che rappresenta la scena (pSurfDataIn) e arriva a ogni punto nello spazio specificato da pSampleLocs. I coefficienti SH rappresentano il mapping, in ogni punto pSampleLocs, della radice di origine alla radice degli eventi imprevisti trasferiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
