---
description: Ottiene un elenco di vertici influenzati da un dato osso e un elenco della quantità di influenza che l'osso ha su ogni vertice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'Metodo ID3DX10SkinInfo:: GetBoneInfluences (D3DX10. h)'
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
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235212"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>Metodo ID3DX10SkinInfo:: GetBoneInfluences

Ottiene un elenco di vertici influenzati da un dato osso e un elenco della quantità di influenza che l'osso ha su ogni vertice.

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

*BoneIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice che specifica un osso esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Offset dalla parte superiore dell'elenco dell'osso dei vertici influenzati. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di indici e pesi da recuperare. Deve essere compreso tra 0 e il valore restituito da ID3DX10SkinInfo:: GetBoneInfluenceCount.

</dd> <dt>

*pDestIndices* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Elenco di indici nel buffer dei vertici, ciascuno dei quali rappresenta un vertice influenzato dall'osso. Questi valori corrispondono ai valori di pDestWeights, in modo che pDestIndices \[ \] corrisponda a pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ in uscita\]
</dt> <dd>

Tipo: **float \***

Elenco della quantità di influenza dell'osso in ogni vertice. Questi valori corrispondono ai valori di pDestIndices, in modo che pDestWeights \[ \] corrisponda a pDestIndices \[ i \] . f

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG o e \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
