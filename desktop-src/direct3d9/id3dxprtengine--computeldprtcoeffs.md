---
description: Consente di calcolare i coefficienti LDPRT (precomputed Radiance Transfer) a livello locale rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati ID3DXPRTBuffer di input.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'Metodo ID3DXPRTEngine:: ComputeLDPRTCoeffs (D3DX9Mesh. h)'
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
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323684"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>Metodo ID3DXPRTEngine:: ComputeLDPRTCoeffs

Consente di calcolare i coefficienti LDPRT (precomputed Radiance Transfer) a livello locale rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input. Questi coefficienti possono essere usati con vettori normali o trasformati per modellare gli effetti globali sugli oggetti dinamici.

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

*pDataIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto dati PRT (pre-Computed Radiance Transfer) di input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*pNormOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Matrice di vettori facoltativa che deve essere riempita con vettori normali ottimali dello shader per i quali sono ottimizzati i coefficienti LDPRT. Questa matrice deve avere le stesse dimensioni del numero di campioni in pDataIn. Se **null**, vengono usati i vettori normali della superficie.

</dd> <dt>

*pDataOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output che contiene i coefficienti armonici di zona dell'ordine per canale di colore per campione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Con questo metodo è possibile ottenere facoltativamente soluzioni per l'ombreggiatura di vettori normali. Questi vettori normali, insieme ai coefficienti LDPRT, possono rappresentare più accuratamente il segnale PRT. In questo caso, i coefficienti rappresentano le armoniche di zona orientate nella direzione normale.

Questo metodo non può essere usato con i risultati di [**ID3DXPRTEngine:: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) o [**ID3DXPRTEngine:: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
