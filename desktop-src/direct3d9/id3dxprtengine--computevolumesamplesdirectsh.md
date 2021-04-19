---
description: Calcola una proiezione di illuminazione distante in vettori di base armonica sferica (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'Metodo ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (D3DX9Mesh. h)'
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
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323451"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>Metodo ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH

Calcola una proiezione di illuminazione distante in vettori di base armonica sferica (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.

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

*Ordinamento* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della rappresentazione SH dell'illuminazione distante. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. Il grado della valutazione è orderin-1.

</dd> <dt>

*Ordinamento* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della rappresentazione SH dell'illuminazione locale. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. Il grado della valutazione è Order out-1.

</dd> <dt>

*NumVolSamples.xml* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di percorsi di esempio.

</dd> <dt>

*pSampleLocs* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posizione per ogni esempio.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che proietta l'illuminazione distante in vettori di base sh. Questo buffer deve avere il numero appropriato di canali di colore allocati per la simulazione. Questo metodo genera un \* ordine in base al secondo per ogni canale in ogni posizione di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo calcola il modo in cui la luce da un'origine distante arriva in ogni punto nello spazio specificato da pSampleLocs. I coefficienti SH rappresentano il mapping, a ogni punto di pSampleLocs, della luminosità del codice sorgente per l'evento imprevisto trasferito.

Per usare correttamente questo metodo, è necessario impostare il campionamento su una sfera con UseSphere = **true** e UseCosine = **false** in [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); in caso contrario, questo metodo restituirà un errore con D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
