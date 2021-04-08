---
description: Applica le grondanze a un oggetto buffer ID3DXPRTBuffer.
ms.assetid: db09aa50-3175-4588-8433-dad6bd37cf0c
title: 'Metodo ID3DXTextureGutterHelper:: ApplyGuttersPRT (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersPRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a99d0cb5d54207d292398468e16b6c35deb4562
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762119"
---
# <a name="id3dxtexturegutterhelperapplyguttersprt-method"></a>Metodo ID3DXTextureGutterHelper:: ApplyGuttersPRT

Applica le grondanze a un oggetto buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ApplyGuttersPRT(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un oggetto buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

I [**Texel della classe 2**](id3dxtexturegutterhelper.md) vengono generati ricampionando la classe 1 e 4 Texel.

La larghezza e l'altezza della trama devono essere uguali a quelle restituite da [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




