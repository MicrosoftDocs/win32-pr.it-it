---
description: Crea una trama del cubo da un file in memoria.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Funzione D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322908"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a>D3DXCreateCubeTextureFromFileInMemory (funzione)

Crea una trama del cubo da un file in memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.

</dd> <dt>

*pSrcData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al file in memoria da cui creare il mappa cubi. Vedere la sezione Osservazioni.

</dd> <dt>

*SrcDataSize* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensioni in byte del file in memoria.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga. Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

La funzione è equivalente a D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppCubeTexture).

Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito. Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.

Questo metodo è progettato per essere usato per il caricamento di file di immagine archiviati come RT \_ RCDATA, ovvero una risorsa definita dall'applicazione (dati non elaborati). In caso contrario, questo metodo avrà esito negativo.

Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo. Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).

**D3DXCreateCubeTextureFromFileInMemory** usa il formato di file DirectDraw Surface (DDS). L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS. È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
