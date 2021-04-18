---
description: Modificare i vertici influenzati da quali ossa.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'Metodo ID3DX10SkinInfo:: RemapVertices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322737"
---
# <a name="id3dx10skininforemapvertices-method"></a>Metodo ID3DX10SkinInfo:: RemapVertices

Modificare i vertici influenzati da quali ossa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewVertexCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nuovo numero di vertici.

</dd> <dt>

*pVertexRemap* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di indici dei vertici, che descrivono la modifica del mapping. Si immagini, ad esempio, che SkinInfo contenga alcuni vertici in modo che bone0 sia mappato a V0, bone1 a V1 e bone2 a V2 e che sia specificata una matrice con 2, 1, 0 per pBoneRemap. In questo modo verrà eseguito il mapping di bone0 a V2, da bone1 a V1 e da bone2 a V0.

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

 

 
