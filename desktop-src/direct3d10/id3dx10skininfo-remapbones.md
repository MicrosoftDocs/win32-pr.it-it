---
description: Modificare le ossa che influenzano i vertici.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'Metodo ID3DX10SkinInfo:: RemapBones (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322738"
---
# <a name="id3dx10skininforemapbones-method"></a>Metodo ID3DX10SkinInfo:: RemapBones

Modificare le ossa che influenzano i vertici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewBoneCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nuovo numero di ossa.

</dd> <dt>

*pBoneRemap* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di indici di osso, che descrivono la modifica del mapping. Si immagini, ad esempio, che SkinInfo contiene alcune ossa in modo che bone0 sia mappato a V0, bone1 a V1 e bone2 a V2 e che sia specificata una matrice con 2, 1, 0 per pBoneRemap. In questo modo verrà eseguito il mapping di bone0 a V2, da bone1 a V1 e da bone2 a V0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory o e \_ INVALIDARG.

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

 

 
