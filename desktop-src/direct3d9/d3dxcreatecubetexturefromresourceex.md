---
description: Crea una trama del cubo da una risorsa specificata da una stringa. Si tratta di una funzione più avanzata rispetto a D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Funzione D3DXCreateCubeTextureFromResourceEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8548863f7c35ff3d56fd83287cf1c3628bb1a9ff89d8ad34346530063c494c99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857301"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a>Funzione D3DXCreateCubeTextureFromResourceEx

Crea una trama del cubo da una risorsa specificata da una stringa. Si tratta di una funzione più avanzata rispetto [**a D3DXCreateCubeTextureFromResource.**](d3dxcreatecubetexturefromresource.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama del cubo.

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

*Dimensioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza e altezza della trama del cubo, in pixel. Ad esempio, se la trama del cubo è un cubo di 8 pixel per 8 pixel, il valore per questo parametro deve essere 8. Se questo valore è 0 o D3DX \_ DEFAULT, le dimensioni vengono prelevate dal file.

</dd> <dt>

*MipLevels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di livelli mip richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0 o D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC. L'impostazione di questo flag su D3DUSAGE RENDERTARGET indica che la \_ superficie deve essere usata come destinazione di rendering. La risorsa può quindi essere passata al *parametro pNewRenderTarget* del [**metodo SetRenderTarget.**](/windows/desktop/api) Se si specifica D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione \_ chiamando [**CheckDeviceFormat.**](/windows/desktop/api) D3DUSAGE \_ DYNAMIC indica che la superficie deve essere gestita in modo dinamico. Per altre informazioni sull'uso di trame dinamiche, vedere [Uso di trame dinamiche.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo [enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel richiesto per la trama del cubo. La trama del cubo restituita potrebbe avere un formato diverso da quello specificato da *Format*. Le applicazioni devono controllare il formato della trama del cubo restituita. Se [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), il formato viene tratto dal file . Se D3DFMT FROM FILE, il formato viene preso esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità \_ \_ del dispositivo.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo [**enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama del cubo.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX, \_ ](d3dx-filter.md)che controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a specificare \_ D3DX \_ \_ FILTER TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*Filtro mip* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine. Specificare D3DX \_ DEFAULT per questo parametro equivale a specificare D3DX FILTER \_ \_ BOX.

</dd> <dt>

*ColorKey* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore. Si tratta sempre di un colore ARGB a 32 bit, indipendentemente dal formato dell'immagine di origine. Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con una descrizione dei dati nel file di immagine di origine oppure **NULL.**

</dd> <dt>

*pPalette* \[ Cambio\]
</dt> <dd>

Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Puntatore a [**una struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza di 256 colori da compilare o **NULL.**

</dd> <dt>

*ppCubeTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) che rappresenta l'oggetto trama del cubo creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromResourceExW.** In caso contrario, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromResourceExA** perché vengono usate stringhe ANSI.

Questa funzione supporta i formati di file seguenti: .bmp, dds, dib, hdr, .jpg, pfm, .png, ppm e tga. Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Le trame dei cubi differiscono dalle altre superfici perché sono raccolte di superfici. Per chiamare [**SetRenderTarget**](/windows/desktop/api) con una trama del cubo, è necessario selezionare un singolo viso usando [**GetCubeMapSurface e**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) passare la superficie risultante a **SetRenderTarget.**

**D3DXCreateCubeTextureFromResourceEx** usa il formato di file DDS (Surface) DirectDraw. L'editor di trama DirectX (Dxtex.exe) consente di generare una mappa cubo da altri formati di file e di salvarla nel formato di file DDS. È possibile ottenere Dxtex.exe informazioni da DirectX SDK. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
