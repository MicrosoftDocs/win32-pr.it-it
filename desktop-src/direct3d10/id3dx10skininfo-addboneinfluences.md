---
description: Consentire a un osso esistente di influenzare un gruppo di vertici e definire la quantità di influenza dell'osso su ogni vertice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'Metodo ID3DX10SkinInfo:: AddBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235034"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>Metodo ID3DX10SkinInfo:: AddBoneInfluences

Consentire a un osso esistente di influenzare un gruppo di vertici e definire la quantità di influenza dell'osso su ogni vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BoneIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice che specifica un osso esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici da aggiungere all'influenza dell'osso.

</dd> <dt>

*pIndices* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di indici di vertice. Ogni membro di questa matrice ha un membro corrispondente in pWeights, in modo che pIndices \[ i \] corrisponda a pWeights \[ i \] . Il valore corrispondente in pWeights \[ \] determina la quantità di influenza che BoneIndex avrà sul vertice indicizzato da pIndices \[ i \] . La dimensione della matrice pIndices deve essere maggiore o uguale a InfluenceCount.

</dd> <dt>

*pWeights* \[ in\]
</dt> <dd>

Tipo: **float \***

Puntatore a una matrice di pesi ossei. Ogni membro di questa matrice ha un membro corrispondente in pIndices, in modo che pWeights \[ i \] corrisponda a pIndices \[ i \] . Ogni valore in pWeights è compreso tra 0 e 1 e definisce la quantità di influenza che l'osso ha su ogni vertice. La dimensione di pWeights deve essere maggiore o uguale a InfluenceCount.

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

 

 
