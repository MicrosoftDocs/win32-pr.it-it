---
description: Trovare l'indice che indica la posizione in cui un vertice specificato si trova in un elenco di vertici influenzato di un dato osso.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'Metodo ID3DX10SkinInfo:: FindBoneInfluenceIndex (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235111"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a>Metodo ID3DX10SkinInfo:: FindBoneInfluenceIndex

Trovare l'indice che indica la posizione in cui un vertice specificato si trova in un elenco di vertici influenzato di un dato osso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BoneIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice che specifica un osso esistente. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*VertexIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice del vertice nel buffer del vertice.

</dd> <dt>

*pInfluenceIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Indice del vertice nell'elenco dell'osso dei vertici influenzati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

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

 

 
