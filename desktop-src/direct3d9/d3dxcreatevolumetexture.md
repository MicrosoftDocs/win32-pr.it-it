---
description: Crea una trama di volume vuota, regolando i parametri chiamanti in base alle esigenze.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Funzione D3DXCreateVolumeTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa3e7b701649b07a9a6da9c0faeed6e0594d1c0e145126c533f87e06249fb8c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119280"
---
# <a name="d3dxcreatevolumetexture-function"></a>Funzione D3DXCreateVolumeTexture

Crea una trama di volume vuota, regolando i parametri chiamanti in base alle esigenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama del volume.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza in pixel. Questo valore deve essere diverso da zero. La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altezza in pixel. Questo valore deve essere diverso da zero. La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Profondità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Profondità in pixel. Questo valore deve essere diverso da zero. La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*MipLevels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di livelli mip richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o D3DUSAGE \_ DYNAMIC. Per altre informazioni sull'uso di trame dinamiche, vedere [Uso di trame dinamiche.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo [enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel richiesto per la trama del volume. La trama del volume restituita potrebbe avere un formato diverso da quello specificato da Formato. Le applicazioni devono controllare il formato della trama del volume restituita.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama del volume.

</dd> <dt>

*ppVolumeTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta l'oggetto trama del volume creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY .

## <a name="remarks"></a>Commenti

Internamente, D3DXCreateVolumeTexture usa [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) per modificare i parametri chiamanti. Di conseguenza, le chiamate a D3DXCreateVolumeTexture avranno spesso esito positivo in caso di esito negativo delle chiamate a [**CreateVolumeTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
