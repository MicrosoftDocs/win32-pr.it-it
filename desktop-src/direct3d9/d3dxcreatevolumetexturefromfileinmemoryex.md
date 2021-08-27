---
description: Crea una trama del volume da un file. Si tratta di una funzione più avanzata rispetto a D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: Funzione D3DXCreateVolumeTextureFromFileInMemoryEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8e273cbdb8e65d751cad4679e7c8a38ec5de2ea2e7e6a62f59d396d44ead24a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119241"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a>Funzione D3DXCreateVolumeTextureFromFileInMemoryEx

Crea una trama del volume da un file. Si tratta di una funzione più avanzata [**di D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al file in memoria da cui creare la trama del volume.

</dd> <dt>

*SrcDataSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Dimensioni del file in memoria, in byte.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza in pixel. Se questo valore è zero o D3DX \_ DEFAULT, le dimensioni vengono prese dal file. La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altezza, in pixel. Se questo valore è zero o D3DX \_ DEFAULT, le dimensioni vengono prese dal file. La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Profondità* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Profondità, in pixel. Se questo valore è zero o D3DX \_ DEFAULT, le dimensioni vengono prese dal file. La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*MipLevels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di livelli mip richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC. L'impostazione di questo flag su D3DUSAGE RENDERTARGET indica che la superficie \_ deve essere usata come destinazione di rendering. La risorsa può quindi essere passata al *parametro pNewRenderTarget* del [**metodo SetRenderTarget.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) Se si specifica D3DUSAGE RENDERTARGET o D3DUSAGE DYNAMIC, il pool deve essere impostato su D3DPOOL DEFAULT e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando \_ \_  \_ [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ DYNAMIC indica che la superficie deve essere gestita dinamicamente. Per altre informazioni sull'uso di trame dinamiche, vedere [Uso di trame dinamiche.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel richiesto per la trama. La trama restituita potrebbe avere un formato diverso da quello specificato da *Format*. Le applicazioni devono controllare il formato della trama restituita. Se [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), il formato viene tratto dal file. Se D3DFMT FROM FILE, il formato viene preso esattamente come si trova nel file e la chiamata avrà esito negativo se viola \_ \_ le funzionalità del dispositivo.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a specificare \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a \_ specificare D3DX \_ FILTER \_ BOX. Usare anche i bit da 27 a 31 per specificare il numero di livelli mip da ignorare (dall'inizio della catena mipmap) quando una trama .dds viene caricata in memoria. In questo modo è possibile ignorare fino a 32 livelli.

</dd> <dt>

*ColorKey* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore. Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato dell'immagine di origine. Alpha è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con una descrizione dei dati nel file di immagine di origine oppure **NULL.**

</dd> <dt>

*pPalette* \[ Cambio\]
</dt> <dd>

Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Puntatore a [**una struttura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza di 256 colori da compilare oppure **NULL.**

</dd> <dt>

*ppVolumeTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione supporta i formati di file .bmp, dds, dib, hdr, .jpg, pfm, .png, ppm e tga. Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Quando si ignorano i livelli mipmap durante il caricamento di un file DDS, usare la macro D3DX SKIP DDS MIP LEVELS per generare \_ \_ il valore \_ \_ *MipFilter.* Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che verrà quindi passato nel *parametro MipFilter.*

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

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
