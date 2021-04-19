---
description: Ottiene il numero di vertici influenzati da un determinato osso.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'Metodo ID3DX10SkinInfo:: GetBoneInfluenceCount (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322743"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a>Metodo ID3DX10SkinInfo:: GetBoneInfluenceCount

Ottiene il numero di vertici influenzati da un determinato osso.

## <a name="syntax"></a>Sintassi


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BoneIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice che specifica un osso esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG.

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

 

 
