---
description: Crea una trama del volume da un file.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Funzione D3DXCreateVolumeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d63377394dc123defac565cd11a0d40324a28a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354899"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a>D3DXCreateVolumeTextureFromFileEx (funzione)

Crea una trama del volume da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pSrcFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*Larghezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Larghezza in pixel. Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file. La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Altezza* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altezza, in pixel. Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file. La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*Profondità* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Profondità, in pixel. Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file. La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

*MipLevels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di livelli MIP richiesti. Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic. L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering. La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . Se \_ viene specificato D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente. Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).

</dd> <dt>

*Formato* 
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama. La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*. Le applicazioni devono verificare il formato della trama restituita. Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file. Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.

</dd> <dt>

*Pool* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.

</dd> <dt>

*Filtro* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata. Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata. La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ . Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.

</dd> <dt>

*ColorKey* \[ in\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey. Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine. Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) da compilare con una descrizione dei dati nel file di immagine di origine o **null**.

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileExW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileExA perché vengono utilizzate le stringhe ANSI.

Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga. Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

Le trame mipmap dispongono automaticamente di ogni livello riempito con la trama del volume caricato. Quando si caricano immagini in trame mipmap, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo. In tal caso, è necessario caricare le immagini manualmente.

Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore *MipFilter* . Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro *MipFilter* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
