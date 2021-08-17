---
title: D3DX11_IMAGE_LOAD_INFO struttura (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Facoltativamente, fornire informazioni alle API del caricatore di trame per controllare la modalità di caricamento delle trame. | D3DX11_IMAGE_LOAD_INFO struttura (D3DX11tex.h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO struttura Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO puntatore alla struttura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45bc3b9ec948c869b121190f52435a257141f1e5a6e9f36c347ab29bafb5522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536858"
---
# <a name="d3dx11_image_load_info-structure"></a>Struttura D3DX11 \_ IMAGE \_ LOAD \_ INFO

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Facoltativamente, fornire informazioni alle API del caricatore di trame per controllare la modalità di caricamento delle trame. Il valore D3DX11 DEFAULT per uno di questi parametri determina l'uso automatico del valore del file di origine da parte di \_ D3DX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Larghezza di destinazione della trama. Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Altezza di destinazione della trama. Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondità della trama. Questo vale solo per le trame di volume.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Livello mipmap con risoluzione più alta della trama. Se è maggiore di 0, dopo il caricamento della trama FirstMipLevel verrà eseguito il mapping al livello mipmap 0.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero massimo di livelli mipmap nella trama. Vedere le osservazioni in [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Se si usa 0 o D3DX11 DEFAULT, verrà creata una catena \_ mipmap completa.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

Modalità di utilizzo della risorsa trama. Vedere [**D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Fasi della pipeline a cui sarà consentita l'associazione della trama. Vedere [**D3D11 \_ BIND \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Autorizzazioni di accesso che la cpu avrà per la risorsa trama. Vedere [**D3D11 \_ CPU ACCESS \_ \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Proprietà delle risorse varie (vedere [**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Enumerazione [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) che indica il formato in cui si trova la trama dopo il caricamento.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtrare la trama usando il filtro specificato (solo durante il ricampionamento). Vedere [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtrare i livelli mip della trama usando il filtro specificato (solo se si generano mipmap). I valori validi sono D3DX11 \_ FILTER \_ NONE, D3DX11 \_ FILTER \_ POINT, D3DX11 \_ FILTER LINEAR o \_ D3DX11 \_ FILTER \_ TRIANGLE. Vedere [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

</dd> <dd>

Informazioni sull'immagine originale. Vedere [**D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md). È possibile ottenere con [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si inizializza la struttura, è possibile impostare qualsiasi membro su D3DX11 DEFAULT e D3DX la inizializza con un valore predefinito dalla trama di origine quando la trama viene \_ caricata.

Questa struttura può essere usata dalle API che:

-   Creare risorse, ad esempio [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).
-   Creare processori di dati, ad esempio [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) o [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).

I valori predefiniti sono:


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



Ecco un breve esempio che usa questa struttura per fornire il formato pixel durante il caricamento di una trama. Per il codice completo, vedere HDRFormats10.cpp [nell'esempio HDRToneMappingCS11.](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx)


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

