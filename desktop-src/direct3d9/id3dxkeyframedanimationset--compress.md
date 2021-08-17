---
description: Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer in cui sono archiviati i dati compressi.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: Metodo ID3DXKeyframedAnimationSet::Compress (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d444ffde525677715f64bd9641cc8fb3cf9513e2c8805a6be28b280aaa12e015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802388"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>Metodo ID3DXKeyframedAnimationSet::Compress

Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer in cui sono archiviati i dati compressi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uno dei valori [**D3DXCOMPRESSION \_ FLAGS**](./d3dxcompression-flags.md) che definiscono la modalità di compressione usata per l'archiviazione dei dati dei set di animazioni compressi. D3DXCOMPRESS \_ DEFAULT è l'unico valore attualmente supportato.

</dd> <dt>

*Perdita di dati* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Rapporto di perdita di compressione desiderato, compreso tra 0 e 1.

</dd> <dt>

*pHierarchy* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntatore a una gerarchia di frame di trasformazione [**D3DXFRAME.**](d3dxframe.md) Può essere **NULL.**

</dd> <dt>

*ppCompressedData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore al set [**di animazioni compresse ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
