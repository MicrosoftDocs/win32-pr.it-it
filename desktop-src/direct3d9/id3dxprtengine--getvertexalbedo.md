---
description: Recupera i valori albedo dei vertici della mesh.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: Metodo ID3DXPRTEngine::GetVertexAlbedo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bdaf264e887c12b6dd711be978c5fc233bacc14d41d0899ddda43473001fe6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985561"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a>Metodo ID3DXPRTEngine::GetVertexAlbedo

Recupera i valori albedo dei vertici della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVertColors* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntatore a una matrice di destinazione di valori albedo dei vertici della mesh. Vedere [**D3DXCOLOR**](d3dxcolor.md).

</dd> <dt>

*NumVerts* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici nella mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
