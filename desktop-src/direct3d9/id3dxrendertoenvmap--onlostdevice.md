---
description: Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'Metodo ID3DXRenderToEnvMap:: OnLostDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b644ab595fd8bc6ebdfa544cc004598f5570d262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354524"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a>Metodo ID3DXRenderToEnvMap:: OnLostDevice

Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente chiami [**IDirect3DDevice9:: Reset**](/windows/desktop/api). Anche se il dispositivo non è stato effettivamente perso, **ID3DXRenderToEnvMap:: OnLostDevice** è responsabile della liberazione di stateblocks e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo. Di conseguenza, non è possibile usare nuovamente l'oggetto Font prima di chiamare **IDirect3DDevice9:: Reset** , quindi [**ID3DXRenderToEnvMap:: OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




