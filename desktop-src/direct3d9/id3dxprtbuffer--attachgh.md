---
description: Associa un oggetto ID3DXTextureGutterHelper all'oggetto ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'Metodo ID3DXPRTBuffer:: AttachGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323046"
---
# <a name="id3dxprtbufferattachgh-method"></a>Metodo ID3DXPRTBuffer:: AttachGH

Associa un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PGH* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Puntatore all'interfaccia [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) di un oggetto che contiene dati di rilegatura della trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.

## <a name="remarks"></a>Commenti

Il conteggio dei riferimenti dell'oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) verrà automaticamente incrementato di uno. Verranno rilasciati tutti i puntatori **ID3DXTextureGutterHelper** esistenti.

È necessario assicurarsi che il numero di chiamate a **ID3DXPRTBuffer:: AttachGH** corrisponda al numero di chiamate a [**ID3DXPRTBuffer:: ReleaseGH**](id3dxprtbuffer--releasegh.md) . Dopo la chiamata a **ID3DXPRTBuffer:: ReleaseGH**, il puntatore PGH restituito da **ID3DXPRTBuffer:: AttachGH** non deve più essere utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




