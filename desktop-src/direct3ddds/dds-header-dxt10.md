---
title: Struttura DDS_HEADER_DXT10 (DDS. h)
description: Estensione dell'intestazione DDS per gestire matrici di risorse, formati pixel DXGI che non vengono mappati alle strutture legacy di formato pixel di Microsoft DirectDraw e metadati aggiuntivi.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- Struttura DDS_HEADER_DXT10 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322293"
---
# <a name="dds_header_dxt10-structure"></a>\_Struttura DXT10 dell'intestazione DDS \_

Estensione dell'intestazione DDS per gestire matrici di risorse, formati pixel DXGI che non vengono mappati alle strutture legacy di formato pixel di Microsoft DirectDraw e metadati aggiuntivi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a>Members

<dl> <dt>

**dxgiFormat**
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Formato pixel della superficie (vedere [**il \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Tipo: **[ **\_ \_ dimensione della risorsa D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifica il tipo di risorsa. I valori seguenti per questo membro sono un subset dei valori nell'enumerazione della dimensione della [**\_ risorsa D3D10 \_**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) o della [**\_ \_ dimensione della risorsa d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :



| Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                            | Valore |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_Dimensione DDS \_ TEXTURE1D ( \_ dimensione risorsa \_ D3D10 \_ TEXTURE1D) | La risorsa è una [trama 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types). Il membro **dwWidth** dell' [**\_ intestazione DDS**](dds-header.md) specifica le dimensioni della trama. In genere, il membro **dwHeight** dell' **\_ intestazione DDS** viene impostato su 1. è necessario impostare anche il \_ flag di altezza DDSD  nel membro dwFlags **dell' \_ intestazione DDS**.                      | 2     |
| \_Dimensione DDS \_ TEXTURE2D ( \_ dimensione risorsa \_ D3D10 \_ TEXTURE2D) | Resource è una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un'area specificata dai membri **dwWidth** e **dwHeight** dell' [**\_ intestazione DDS**](dds-header.md). È anche possibile usare questo tipo per identificare una trama del mapping del cubo. Per ulteriori informazioni sull'identificazione di una trama con mappa cubo, vedere **miscFlag** e **arraySize** members. | 3     |
| \_Dimensione DDS \_ TEXTURE3D ( \_ dimensione risorsa \_ D3D10 \_ TEXTURE3D) | Resource è una [trama 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un volume specificato dai membri **dwWidth**, **DwHeight** e **dwDepth** dell' [**\_ intestazione DDS**](dds-header.md). È anche necessario impostare il \_ flag di profondità DDSD nel membro **dwFlags** dell' **\_ intestazione DDS**.                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifica altre opzioni meno comuni per le risorse. Il valore seguente per questo membro è un subset dei valori nel [**\_ \_ \_ flag misc della risorsa D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) o nell'enumerazione del [**\_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :



| Tipo                             | Descrizione                                                                                                  | Valore |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| \_risorsa DDS \_ \_ TEXTURECUBE varie | Indica che una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) è una trama con mappa cubo. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi nella matrice.

Per una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) che è anche una trama con mappa cubo, questo numero rappresenta il numero di cubi. Questo numero corrisponde al numero nel membro **NumCubes** di [**D3D10 \_ TEXCUBE \_ array \_ srv1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) o [**d3d11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). In questo caso, il file DDS contiene **arraySize** \* 6 trame 2D. Per ulteriori informazioni su questo caso, vedere la descrizione di **miscFlag** .

Per una [trama 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), è necessario impostare questo numero su 1.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Contiene metadati aggiuntivi (in precedenza è stato riservato). I 3 bit inferiori indicano la modalità Alpha della risorsa associata. I 29 bit superiori sono riservati e sono in genere 0.



| Tipo                            | Descrizione                                                                                                                              | Valore |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_modalità Alpha \_ DDS \_ sconosciuta       | Il contenuto del canale alfa è sconosciuto. Si tratta del valore per i file legacy, che in genere si presuppone essere "Alpha".                 | 0x0   |
| \_modalità Alpha \_ DDS \_ diritta      | Si presume che il contenuto del canale alfa usi un Alpha diretto.                                                                             | 0x1   |
| \_modalità alfa \_ DDS \_ premoltiplicata | Qualsiasi contenuto del canale alfa utilizza un alfa premoltiplicato. Gli unici formati di file legacy che indicano queste informazioni sono ' DX2' è DX4'. | 0x2   |
| \_opaco in \_ modalità \_ Alpha DDS        | Tutti i contenuti del canale alfa sono tutti impostati su completamente opachi.                                                                                    | 0x3   |
| \_personalizzazione della \_ modalità \_ Alpha DDS        | Qualsiasi contenuto del canale alfa viene usato come quarto canale e non è destinato a rappresentare la trasparenza (diritta o premoltiplicata).      | 0x4   |



 

> [!Note]  
> Le librerie di utilità legacy D3DX 10 e [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) non verranno caricate. Il file DDS con **miscFlags2** non è uguale a zero.

 

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questa struttura insieme a un' [**\_ intestazione DDS**](dds-header.md) per archiviare una matrice di risorse in un file DDS. Per altre informazioni, vedere [matrici di trame](dx-graphics-dds-pguide.md).

Questa intestazione è presente se il membro **dwFourCC** della struttura del gruppo di test di [**DDS \_**](dds-pixelformat.md) è impostato su' DX10'.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento per DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

