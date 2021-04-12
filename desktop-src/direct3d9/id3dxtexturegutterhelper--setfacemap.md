---
description: Imposta l'indice della faccia mesh a cui appartiene ogni Texel.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'Metodo ID3DXTextureGutterHelper:: SetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235161"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>Metodo ID3DXTextureGutterHelper:: SetFaceMap

Imposta l'indice della faccia mesh a cui appartiene ogni Texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFaceData* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore all'indice della faccia mesh a cui appartiene ogni Texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

L'input dei dati della faccia mesh per questo metodo è valido solo per Texel validi (non di classe 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i Texel validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
