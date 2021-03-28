---
title: Struttura D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. | Struttura D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- Struttura D3DX11_IMAGE_LOAD_INFO Direct3D 11
- Puntatore alla struttura LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
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
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982555"
---
# <a name="d3dx11_image_load_info-structure"></a>\_Struttura delle \_ informazioni sul caricamento dell'immagine D3DX11 \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. Il valore predefinito D3DX11 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Larghezza di destinazione della trama. Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Altezza di destinazione della trama. Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondità della trama. Questo vale solo per le trame del volume.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Livello di mipmap di risoluzione più alto della trama. Se è maggiore di 0, dopo il caricamento della trama FirstMipLevel verrà eseguito il mapping a mipmap livello 0.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero massimo di livelli di mipmap nella trama. Vedere la sezione Osservazioni in [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Se \_ si usa il valore predefinito 0 o D3DX11, verrà creata una catena mipmap completa.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **\_ utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

Il modo in cui la risorsa di trama deve essere utilizzata. Vedere [**\_ utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Fasi della pipeline a cui sarà consentita l'associazione della trama. Vedere [**\_ \_ flag di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Autorizzazioni di accesso che la CPU avrà per la risorsa di trama. Vedere [**\_ flag di \_ accesso \_ alla CPU d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Proprietà delle risorse varie ( [**vedere \_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Enumerazione [**del \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) che indica il formato in cui si troverà la trama dopo il caricamento.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtrare la trama usando il filtro specificato (solo quando si esegue il ricampionamento). Vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtrare i livelli MIP della trama usando il filtro specificato (solo se si sta generando mipmap). I valori validi sono D3DX11 \_ Filter \_ None, D3DX11 Filter \_ \_ Point, D3DX11 \_ Filter \_ Linear o D3DX11 \_ Filter \_ Triangle. Vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ info**](d3dx11-image-info.md)\***

</dd> <dd>

Informazioni sull'immagine originale. Vedere [**D3DX11 \_ Image \_ info**](d3dx11-image-info.md). Può essere ottenuto con [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si inizializza la struttura, è possibile impostare qualsiasi membro su D3DX11 \_ default e D3DX lo inizializza con un valore predefinito dalla trama di origine quando viene caricata la trama.

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



Ecco un breve esempio che usa questa struttura per fornire il formato pixel durante il caricamento di una trama. Per il codice completo, vedere l'esempio HDRFormats10. cpp in [HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


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
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

