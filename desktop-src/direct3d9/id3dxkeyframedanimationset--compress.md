---
description: Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer che archivia i dati compressi.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Metodo ID3DXKeyframedAnimationSet:: Compress (D3dx9anim. h)'
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
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323530"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>Metodo ID3DXKeyframedAnimationSet:: Compress

Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer che archivia i dati compressi.

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

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uno dei valori [**di \_ flag D3DXCOMPRESSION**](./d3dxcompression-flags.md) che definiscono la modalità di compressione utilizzata per l'archiviazione dei dati del set di animazioni compressi. \_Il valore predefinito di D3DXCOMPRESS è l'unico valore attualmente supportato.

</dd> <dt>

*Lossiness* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Percentuale di perdita di compressione desiderata nell'intervallo compreso tra 0 e 1.

</dd> <dt>

*pHierarchy* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Puntatore a una gerarchia del frame di trasformazione [**D3DXFRAME**](d3dxframe.md) . Può essere **null**.

</dd> <dt>

*ppCompressedData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore al set di animazioni compresso [**ID3DXBuffer**](id3dxbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
