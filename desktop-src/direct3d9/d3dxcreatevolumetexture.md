---
description: Crea una trama del volume vuota, modificando i parametri di chiamata in base alle esigenze.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Funzione D3DXCreateVolumeTexture (D3dx9tex. h)
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
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969359"
---
# <a name="d3dxcreatevolumetexture-function"></a>D3DXCreateVolumeTexture (funzione)

Crea una trama del volume vuota, modificando i parametri di chiamata in base alle esigenze.

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

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.

</dd> <dt>

*Larghezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Larghezza in pixel. Questo valore deve essere diverso da zero. La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Altezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altezza in pixel. Questo valore deve essere diverso da zero. La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Profondità* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Profondità in pixel. Questo valore deve essere diverso da zero. La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*MipLevels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di livelli MIP richiesti. Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o D3DUSAGE \_ dinamico. Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).

</dd> <dt>

*Formato* \[ in\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama del volume. Il formato della trama del volume restituito può essere diverso da quello specificato dal formato. Le applicazioni devono controllare il formato della trama del volume restituito.

</dd> <dt>

*Pool* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del volume.

</dd> <dt>

*ppVolumeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama del volume creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Internamente, D3DXCreateVolumeTexture USA [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) per modificare i parametri di chiamata. Di conseguenza, le chiamate a D3DXCreateVolumeTexture avranno spesso esito positivo laddove le chiamate a [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) non riusciranno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
