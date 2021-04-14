---
description: Annulla l'associazione di un oggetto ID3DXTextureGutterHelper associato all'oggetto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'Metodo ID3DXPRTBuffer:: ReleaseGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402028"
---
# <a name="id3dxprtbufferreleasegh-method"></a>Metodo ID3DXPRTBuffer:: ReleaseGH

Annulla l'associazione di un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) associato all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo rilascia il puntatore all'interfaccia [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

È necessario assicurarsi che il numero di chiamate a [**ID3DXPRTBuffer:: AttachGH**](id3dxprtbuffer--attachgh.md) corrisponda al numero di chiamate a **ID3DXPRTBuffer:: ReleaseGH** . Dopo la chiamata a **ID3DXPRTBuffer:: ReleaseGH**, il puntatore PGH restituito da **ID3DXPRTBuffer:: AttachGH** non deve più essere utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




