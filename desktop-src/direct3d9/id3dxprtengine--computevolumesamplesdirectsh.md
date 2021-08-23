---
description: Calcola una proiezione di illuminazione distante in vettori di base sferici aricali (SH) che rappresentano la luminosità degli eventi imprevisti in posizioni specificate.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: Metodo ID3DXPRTEngine::ComputeVolumeSamplesDirectSH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3aaa8f9332a80e35ffde43d145be1ed885caeaca6d61e4eb9190baba09b73ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747761"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>Metodo ID3DXPRTEngine::ComputeVolumeSamplesDirectSH

Calcola una proiezione di illuminazione distante in vettori di base sferici aricali (SH) che rappresentano la luminosità degli eventi imprevisti in posizioni specificate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OrderIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della rappresentazione SH dell'illuminazione distante. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. Il grado di valutazione è OrderIn - 1.

</dd> <dt>

*OrderOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della rappresentazione SH dell'illuminazione locale. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. Il grado di valutazione è OrderOut - 1.

</dd> <dt>

*NumVolSamples.xml* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di posizioni di esempio.

</dd> <dt>

*pSampleLocs* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posizione per ogni campione.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che proietta l'illuminazione distante in vettori di base SH. Questo buffer deve avere il numero corretto di canali di colore allocati per la simulazione. Questo metodo genera valori \* scalari OrderIn più ordinabili per canale in ogni posizione di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo calcola il modo in cui la luce da un'origine distante arriva in ogni punto dello spazio specificato da pSampleLocs. I coefficienti SH rappresentano il mapping, in ogni punto pSampleLocs, della radice di origine alla radice degli eventi imprevisti trasferiti.

Per usare correttamente questo metodo, è necessario impostare il campionamento su una sfera con UseSphere = **TRUE** e UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); In caso contrario, questo metodo restituirà un errore con D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
