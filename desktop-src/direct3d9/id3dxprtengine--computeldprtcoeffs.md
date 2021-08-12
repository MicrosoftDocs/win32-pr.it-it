---
description: Calcola i coefficienti LDPRT (Precomputed Radiance Transfer) locali rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati ID3DXPRTBuffer di input.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: Metodo ID3DXPRTEngine::ComputeLDPRTCoeffs (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a432f1df1ad905ca3200789aa6245212cc180d4c7ef5a8723cf02695aeeb7454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294037"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>Metodo ID3DXPRTEngine::ComputeLDPRTCoeffs

Calcola i coefficienti LDPRT (Precomputed Radiance Transfer) locali rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input. Questi coefficienti possono essere usati con vettori normali con interfaccia o trasformati per modellare gli effetti globali sugli oggetti dinamici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDataIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto dati PRT (Pre-Computed Radiance Transfer) Spherical Arance Transfer (SH) spherical pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) precomputed radiance transfer (PRT).

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*pNormOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Matrice di vettori facoltativa da riempire con vettori normali ottimali per lo shader per i quali sono ottimizzati i coefficienti LDPRT. Questa matrice deve avere le stesse dimensioni del numero di campioni in pDataIn. Se **NULL,** vengono usati vettori normali di superficie.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un [**oggetto ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che contiene coefficienti arrillici di zona Order per canale di colore per campione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Le soluzioni per l'ombreggiatura dei vettori normali possono essere ottenute facoltativamente con questo metodo. Questi vettori normali, insieme ai coefficienti LDPRT, possono rappresentare in modo più accurato il segnale PRT. In questo caso, i coefficienti rappresentano gli armeni di zona orientati nella direzione normale.

Questo metodo non può essere usato con i risultati di [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) o [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH.**](id3dxprtengine--computesurfsamplesdirectsh.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
