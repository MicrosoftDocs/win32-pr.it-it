---
description: Crea una trama vuota, modificando i parametri di chiamata in base alle esigenze.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Funzione D3DXCreateTexture (D3dx9tex. h)
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
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530918"
---
# <a name="d3dxcreatetexture-function"></a>D3DXCreateTexture (funzione)

Crea una trama vuota, modificando i parametri di chiamata in base alle esigenze.

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

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*Larghezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Larghezza in pixel. Se questo valore è 0, viene utilizzato il valore 1. Vedere la sezione Osservazioni.

</dd> <dt>

*Altezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altezza in pixel. Se questo valore è 0, viene utilizzato il valore 1. Vedere la sezione Osservazioni.

</dd> <dt>

*MipLevels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di livelli MIP richiesti. Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ Dynamic**. L'impostazione di questo flag su **D3DUSAGE \_ RENDERTARGET** indica che la superficie deve essere utilizzata come destinazione di rendering chiamando il metodo [**SetRenderTarget**](/windows/desktop/api) . Se viene specificato **D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ Dynamic** , l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api). Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).

</dd> <dt>

*Formato* \[ in\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama. Il formato della trama restituita può essere diverso da quello specificato, se il dispositivo non supporta il formato richiesto. Le applicazioni devono controllare il formato della trama restituita per verificare se corrisponde al formato richiesto.

</dd> <dt>

*Pool* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Internamente, D3DXCreateTexture USA [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) per modificare i parametri di chiamata. Di conseguenza, le chiamate a D3DXCreateTexture avranno spesso esito positivo laddove le chiamate a [**createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) non riusciranno.

Se l'altezza e la larghezza sono impostate su [D3DX \_ default](other-d3dx-constants.md), per entrambi i parametri viene utilizzato il valore 256. Se l'altezza o la larghezza è impostata su D3DX \_ default e l'altro parametro è impostato su un valore numerico, la trama sarà quadrata con l'altezza e la larghezza uguali al valore numerico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
