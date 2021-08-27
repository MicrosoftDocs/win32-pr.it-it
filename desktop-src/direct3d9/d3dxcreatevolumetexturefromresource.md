---
description: Crea una trama del volume da una risorsa.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: Funzione D3DXCreateVolumeTextureFromResource (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0d54e4981b9dccf655978df8f08bb9154e41d1ec9918c9a6db0ee65b0be6de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119231"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a>Funzione D3DXCreateVolumeTextureFromResource

Crea una trama del volume da una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama del volume.

</dd> <dt>

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle per il modulo in cui si trova la risorsa o **NULL** per il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome della risorsa. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati string viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppVolumeTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromResourceW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromResourceA perché vengono usate stringhe ANSI.

La funzione è equivalente a D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).

La risorsa caricata deve essere una risorsa definita dall'applicazione (RT \_ RCDATA).

Questa funzione supporta i formati di file seguenti: .bmp, dds, dib, hdr, .jpg, pfm, .png, ppm e tga. Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria denotata da D3DPOOL \_ MANAGED. Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria denotata da D3DPOOL \_ DEFAULT.

Il filtro viene applicato automaticamente a una trama creata usando questo metodo. Il filtro equivale a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
