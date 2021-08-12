---
description: Modificare i vertici influenzati da quale gruppo.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: Metodo ID3DX10SkinInfo::RemapVertices (D3DX10.h)
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
ms.openlocfilehash: d73b9878a43ef876174561f16678f78787b15b88f423ecfb3f1765bd82c84630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302477"
---
# <a name="id3dx10skininforemapvertices-method"></a>Metodo ID3DX10SkinInfo::RemapVertices

Modificare i vertici influenzati da quale gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewVertexCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nuovo numero di vertici.

</dd> <dt>

*pVertexRemap* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di indici dei vertici, che descrivono il nuovo mapping. Si supponga, ad esempio, che SkinInfo contenga alcuni vertici, in modo che sia stato eseguito il mapping di 0 a v0, da 1 a v1 e da 2 a v2 e che la matrice con 2,1,0 sia specificata per pBoneRemap. In questo modo verrà eseguito il mapping di a v2, da 1 a v1 e da 2 a v0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ OUTOFMEMORY o E \_ INVALIDARG.

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

 

 
