---
description: Crea una trama da un file. Si tratta di una funzione più avanzata rispetto a D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Funzione D3DXCreateTextureFromFileEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5964f7f466dac135d08958ef66c12a1dfe2e61a19180eb45072c5489f9f4a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299246"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>Funzione D3DXCreateTextureFromFileEx

Crea una trama da un file. Si tratta di una funzione più avanzata di [**D3DXCreateTextureFromFile.**](d3dxcreatetexturefromfile.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pSrcFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati stringa viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza in pixel. Se questo valore è zero o D3DX DEFAULT, le dimensioni vengono prese dal file e arrotondate \_ a una potenza di due. Se il dispositivo supporta la non alimentazione di 2 trame ed è specificato [D3DX \_ DEFAULT \_ NONPOW2,](other-d3dx-constants.md) le dimensioni non verranno arrotondate.

</dd> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altezza, in pixel. Se questo valore è zero o D3DX DEFAULT, le dimensioni vengono prese dal file e arrotondate \_ a una potenza di due. Se il dispositivo supporta la non alimentazione di 2 trame e [D3DX \_ DEFAULT \_ NONPOW2](other-d3dx-constants.md) è sepcificato, le dimensioni non verranno arrotondate.

</dd> <dt>

*MipLevels* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di livelli mip richiesti. Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa. Se D3DX FROM FILE, le dimensioni verranno prese esattamente come nel file e la chiamata avrà esito negativo se viola le funzionalità \_ \_ del dispositivo.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ DYNAMIC.** L'impostazione di questo flag **su D3DUSAGE \_ RENDERTARGET** indica che la superficie deve essere usata come destinazione di rendering. La risorsa può quindi essere passata al *parametro pNewRenderTarget* del [**metodo SetRenderTarget.**](/windows/desktop/api) Se si **specifica D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ DYNAMIC,** *il pool* deve essere impostato su D3DPOOL DEFAULT e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando \_ [**CheckDeviceFormat**](/windows/desktop/api). **D3DUSAGE \_ DYNAMIC** indica che la superficie deve essere gestita dinamicamente. Vedere [Uso di trame dinamiche.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel richiesto per la trama. La trama restituita potrebbe avere un formato diverso da quello specificato da *Format*. Le applicazioni devono controllare il formato della trama restituita. Se D3DFMT \_ UNKNOWN, il formato viene tratto dal file. Se D3DFMT FROM FILE, il formato viene preso esattamente come si trova nel file e la chiamata avrà esito negativo se viola \_ \_ le funzionalità del dispositivo.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama.

</dd> <dt>

*Filtro* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di una o più [costanti FILTER \_ D3DX](d3dx-filter.md) che controllano la modalità di filtro dell'immagine. Specificare [D3DX \_ DEFAULT](other-d3dx-constants.md) per questo parametro equivale a specificare D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di una o più [costanti FILTER \_ D3DX](d3dx-filter.md) che controllano la modalità di filtro dell'immagine. Specificare D3DX DEFAULT per questo parametro equivale a \_ specificare D3DX \_ FILTER \_ BOX. Usare anche i bit da 27 a 31 per specificare il numero di livelli mip da ignorare (dall'inizio della catena mipmap) quando una trama .dds viene caricata in memoria. In questo modo è possibile ignorare fino a 32 livelli.

</dd> <dt>

*ColorKey* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore. Si tratta sempre di un colore ARGB a 32 bit, indipendentemente dal formato dell'immagine di origine. Alpha è significativo e in genere deve essere impostato su FF per le chiavi di colore opache. Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.

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

*ppTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileExW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileExA perché vengono usate stringhe ANSI.

Usare [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) per determinare se il dispositivo può supportare la trama in base allo stato corrente.

Questa funzione supporta i formati di file .bmp, dds, dib, hdr, .jpg, pfm, .png, ppm e tga. Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Le trame mipmapped hanno automaticamente ogni livello riempito con la trama caricata. Quando si caricano immagini in trame mipmapped, alcuni dispositivi non possono passare a un'immagine 1x1 e questa funzione avrà esito negativo. In questo caso, le immagini devono essere caricate manualmente.

Per prestazioni ottimali quando si usa **D3DXCreateTextureFromFileEx**:

1.  L'esecuzione del ridimensionamento delle immagini e della conversione del formato in fase di caricamento può essere lenta. Archiviare le immagini nel formato e nella risoluzione che verranno usate. Se l'hardware di destinazione richiede una potenza di 2 dimensioni, creare e archiviare immagini usando una potenza di 2 dimensioni.
2.  Per la creazione di immagini mipmap in fase di caricamento, filtrare [usando D3DX \_ FILTER \_ BOX](d3dx-filter.md). Un filtro casella è molto più veloce rispetto ad altri tipi di filtro, ad esempio D3DX \_ FILTER \_ TRIANGLE.
3.  Prendere in considerazione l'uso di file DDS. Poiché i file DDS possono essere usati per rappresentare qualsiasi formato di trama Direct3D 9, sono molto facili da leggere per D3DX. Inoltre, possono archiviare mipmap, in modo che qualsiasi algoritmo di generazione mipmap possa essere usato per creare le immagini.

Quando si ignorano i livelli mipmap durante il caricamento di un file DDS, usare la macro D3DX SKIP DDS MIP LEVELS per generare \_ \_ il valore \_ \_ MipFilter. Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che verrà quindi passato nel parametro MipFilter.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
