---
description: Ottiene la quantità di influenza che un determinato sodale ha su un vertice specificato.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: Metodo ID3DX10SkinInfo::GetBoneInfluence (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b53f642b6e62bb37c6979602b1ae66e09ffc2eb42a6d47c70c6b895a01ba273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096551"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>Metodo ID3DX10SkinInfo::GetBoneInfluence

Ottiene la quantità di influenza che un determinato sodale ha su un vertice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IndexIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice che specifica un oggetto esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Indice di influenza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice nell'elenco dei vertici su cui influisce.

</dd> <dt>

*pWeight* \[ Pollici\]
</dt> <dd>

Tipo: **\* float**

La quantità di influenza, compresa tra 0 e 1, che l'abile ha sul vertice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.

## <a name="remarks"></a>Commenti

Usare ID3DX10SkinInfo::GetBoneInfluenceCount per individuare il numero di vertici su cui influisce l'elemento.

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

 

 
