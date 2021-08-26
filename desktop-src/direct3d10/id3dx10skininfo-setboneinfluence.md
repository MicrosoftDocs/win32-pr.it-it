---
description: Consente di impostare la quantità di influenza che ha un'endote su un vertice specificato.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: Metodo ID3DX10SkinInfo::SetBoneInfluence (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1bf2f2a6ec92a1e4551bdc22d43bd143c9da5c8114c44619c073a838de52c606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069961"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a>Metodo ID3DX10SkinInfo::SetBoneInfluence

Consente di impostare la quantità di influenza che ha un'endote su un vertice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
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

*Peso* \[ Pollici\]
</dt> <dd>

Tipo: **float**

La quantità di influenza, compresa tra 0 e 1, che l'abile ha sul vertice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.

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

 

 
