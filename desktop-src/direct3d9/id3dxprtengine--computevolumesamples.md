---
description: Calcola una proiezione dell'illuminazione diretta dal rimbalzo della luce precedente in vettori di base armonici sferici che rappresentano la radianza dell'evento imprevisto nelle posizioni specificate.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'Metodo ID3DXPRTEngine:: ComputeVolumeSamples (D3DX9Mesh. h)'
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
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323452"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>Metodo ID3DXPRTEngine:: ComputeVolumeSamples

Calcola una proiezione dell'illuminazione diretta dal rimbalzo della luce precedente in vettori di base armonici sferici che rappresentano la radianza dell'evento imprevisto nelle posizioni specificate.

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

*pSurfDataIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input che rappresenta l'oggetto 3D del rimbalzo della luce precedente.

</dd> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*NumVolSamples.xml* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di percorsi di esempio.

</dd> <dt>

*pSampleLocs* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posizione per ogni esempio. Se pSampleLocs è **null**, ComputeVolumeSamples calcolerà le matrici di trasferimento a ogni vertice di rete. Tuttavia, se pSampleLocs non è **null**, è necessario campionare su una sfera (set UseSphere = **true** e UseCosine = **false** in [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); in caso contrario, ComputeVolumeSamples restituirà D3DERR \_ INVALIDCALL.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che proietta l'illuminazione diretta dal rimbalzo della luce precedente nei vettori di base sh. Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo calcola il modo in cui la luce della funzione di luminosità di origine viene riflessa dalla superficie che rappresenta la scena (pSurfDataIn) e arriva a ogni punto nello spazio specificato da pSampleLocs. I coefficienti SH rappresentano il mapping, a ogni punto di pSampleLocs, della luminosità del codice sorgente per l'evento imprevisto trasferito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
