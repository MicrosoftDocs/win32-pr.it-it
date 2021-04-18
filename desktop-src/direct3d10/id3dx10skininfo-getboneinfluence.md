---
description: Ottenere la quantità di influenza di un dato osso su un vertice specificato.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'Metodo ID3DX10SkinInfo:: GetBoneInfluence (D3DX10. h)'
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
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323134"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>Metodo ID3DX10SkinInfo:: GetBoneInfluence

Ottenere la quantità di influenza di un dato osso su un vertice specificato.

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

*BoneIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice che specifica un osso esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice nell'elenco di vertici dell'osso che influenza.

</dd> <dt>

*pWeight* \[ in\]
</dt> <dd>

Tipo: **float \***

La quantità di influenza, tra 0 e 1, che l'osso ha sul vertice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.

## <a name="remarks"></a>Commenti

Usare ID3DX10SkinInfo:: GetBoneInfluenceCount per determinare il numero di vertici influenzati dall'osso.

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

 

 
