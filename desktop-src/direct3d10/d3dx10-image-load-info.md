---
description: Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. Il valore predefinito D3DX10 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Struttura D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323323"
---
# <a name="d3dx10_image_load_info-structure"></a>\_Struttura delle \_ informazioni sul caricamento dell'immagine d3dx10 \_

Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. Il valore predefinito D3DX10 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza di destinazione della trama. Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza di destinazione della trama. Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondità della trama. Questo vale solo per le trame del volume.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello di mipmap di risoluzione più alto della trama. Se è maggiore di 0, dopo il caricamento della trama FirstMipLevel verrà eseguito il mapping a mipmap livello 0.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero massimo di livelli di mipmap che avrà la trama. Se \_ si usa il valore predefinito 0 o d3dx10, verrà creata una catena mipmap completa.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **\_ utilizzo di D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

Il modo in cui la risorsa di trama deve essere utilizzata. Vedere [**\_ utilizzo di D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Fasi della pipeline a cui sarà consentita l'associazione della trama. Vedere [**\_ \_ flag di binding D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Autorizzazioni di accesso che la CPU avrà per la risorsa di trama. Vedere [**\_ flag di \_ accesso \_ alla CPU D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Proprietà delle risorse varie ( [**vedere \_ \_ \_ flag varie della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Formato in cui si troverà la trama dopo il caricamento. Vedere [**il \_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtrare la trama usando il filtro specificato (solo quando si esegue il ricampionamento). Vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtrare i livelli MIP della trama usando il filtro specificato (solo se si sta generando mipmap). I valori validi sono D3DX10 \_ Filter \_ None, d3dx10 Filter \_ \_ Point, D3DX10 \_ Filter \_ Linear o d3dx10 \_ Filter \_ Triangle. Vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **d3dx10 \_ Image \_ info**](d3dx10-image-info.md)\***

</dd> <dd>

Informazioni sull'immagine originale. Vedere [**d3dx10 \_ Image \_ info**](d3dx10-image-info.md). Può essere ottenuto con [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)o [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si inizializza la struttura, è possibile impostare qualsiasi membro su D3DX10 \_ default e D3DX lo inizializza con un valore predefinito dalla trama di origine quando viene caricata la trama.

Questa struttura può essere usata dalle API che:

-   Creare risorse, ad esempio [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).
-   Creare processori di dati, ad esempio [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) o [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
