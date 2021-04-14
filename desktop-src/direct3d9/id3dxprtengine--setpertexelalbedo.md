---
description: Imposta un valore albedo per ogni Texel, sovrascrivendo i valori albedo precedenti.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'Metodo ID3DXPRTEngine:: SetPerTexelAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401982"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>Metodo ID3DXPRTEngine:: SetPerTexelAlbedo

Imposta un valore albedo per ogni Texel, sovrascrivendo i valori albedo precedenti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlbedoTexture* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) in cui archiviare i valori albedo.

</dd> <dt>

*NumChannels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di canali dei colori da impostare. Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.

</dd> <dt>

*PGH* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Puntatore facoltativo a un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) . Se non viene specificato, viene creato ed eliminato internamente un oggetto helper di rilegatura della trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASSTILLDRAWING, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
