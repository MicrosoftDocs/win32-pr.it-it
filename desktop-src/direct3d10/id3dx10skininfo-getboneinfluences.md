---
description: Ottenere un elenco di vertici influenzati da una determinata leta e un elenco della quantità di influenza che ha la testa su ogni vertice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: Metodo ID3DX10SkinInfo::GetBoneInfluences (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 38d6901abd871a2b65f4d6816ad4d4b7a0d2effb5ccbd3f4ccee20bc0b8d5ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752911"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>Metodo ID3DX10SkinInfo::GetBoneInfluences

Ottenere un elenco di vertici influenzati da una determinata leta e un elenco della quantità di influenza che ha la testa su ogni vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IndexIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice che specifica un oggetto esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Offset dalla parte superiore dell'elenco dei vertici influenzati. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di indici e pesi da recuperare. Deve essere compreso tra 0 e il valore restituito da ID3DX10SkinInfo::GetBoneInfluenceCount.

</dd> <dt>

*pDestIndices* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Elenco di indici nel buffer dei vertici, ognuno dei quali rappresenta un vertice influenzato dal vertice. Questi valori corrispondono ai valori in pDestWeights, in modo che pDestIndices i corrisponda \[ \] a pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ in, out\]
</dt> <dd>

Tipo: **\* float**

Elenco della quantità di influenza che ha la testa su ogni vertice. Questi valori corrispondono ai valori in pDestIndices, in modo che pDestWeights i corrisponda \[ \] a pDestIndices \[ i \] .f

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG o E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
