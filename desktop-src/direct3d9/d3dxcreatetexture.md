---
description: Crea una trama vuota, regolando i parametri chiamanti in base alle esigenze.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Funzione D3DXCreateTexture (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6264be0712f5ac7f30a9882efde5c66e1e75404634e77d6b72d2313ba016fd6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299256"
---
# <a name="d3dxcreatetexture-function"></a>Funzione D3DXCreateTexture

Crea una trama vuota, regolando i parametri chiamanti in base alle esigenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza in pixel. Se questo valore è 0, viene usato il valore 1. Vedere la sezione Osservazioni.

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altezza in pixel. Se questo valore è 0, viene usato il valore 1. Vedere la sezione Osservazioni.

</dd> <dt>

*MipLevels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di livelli mip richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ DYNAMIC.** L'impostazione di questo flag su **D3DUSAGE \_ RENDERTARGET** indica che la superficie deve essere usata come destinazione di rendering chiamando il [**metodo SetRenderTarget.**](/windows/desktop/api) Se si **specifica D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ DYNAMIC,** l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api). Per altre informazioni sull'uso di trame dinamiche, vedere [Uso di trame dinamiche](performance-optimizations.md).

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel richiesto per la trama. La trama restituita può avere un formato diverso da quello specificato, se il dispositivo non supporta il formato richiesto. Le applicazioni devono controllare il formato della trama restituita per verificare se corrisponde al formato richiesto.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama.

</dd> <dt>

*ppTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Internamente, D3DXCreateTexture usa [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) per modificare i parametri chiamanti. Di conseguenza, le chiamate a D3DXCreateTexture avranno spesso esito positivo in caso di esito negativo [**delle chiamate a CreateTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)

Se sia Height che Width sono impostati su [D3DX \_ DEFAULT,](other-d3dx-constants.md)per entrambi i parametri viene usato il valore 256. Se Height o Width è impostato su D3DX DEFAULT e l'altro parametro è impostato su un valore numerico, la trama sarà quadrata con l'altezza e la larghezza uguali al \_ valore numerico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
