---
description: Annulla l'associazione di un oggetto ID3DXTextureGutterHelper associato all'oggetto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: Metodo ID3DXPRTBuffer::ReleaseGH (D3DX9Mesh.h)
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
ms.openlocfilehash: 5691fc2601624733bb8d41b63140b694bd78027e0f6d548b02984bbc12406a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120535"
---
# <a name="id3dxprtbufferreleasegh-method"></a>Metodo ID3DXPRTBuffer::ReleaseGH

Annulla l'associazione di un [**oggetto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) associato all'oggetto [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

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

Questo metodo rilascia il puntatore [**all'interfaccia ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md)

È necessario assicurarsi che il numero di [**chiamate ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) corrisponda al numero di **chiamate ID3DXPRTBuffer::ReleaseGH.** Dopo aver **chiamato ID3DXPRTBuffer::ReleaseGH,** il puntatore pGH restituito da **ID3DXPRTBuffer::AttachGH** non deve più essere usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




