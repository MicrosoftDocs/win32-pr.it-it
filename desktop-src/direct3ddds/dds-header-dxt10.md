---
title: DDS_HEADER_DXT10 struttura (Dds.h)
description: Estensione dell'intestazione DDS per gestire le matrici di risorse, i formati pixel DXGI che non esempe il mapping alle strutture di formato pixel di Microsoft DirectDraw legacy e metadati aggiuntivi.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 struttura DDS
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
ms.openlocfilehash: 9da95b65739922861002ab134d33f276adabd19c29d14fdea6432616b6c5edc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289788"
---
# <a name="dds_header_dxt10-structure"></a>Struttura DDS \_ HEADER \_ DXT10

Estensione dell'intestazione DDS per gestire le matrici di risorse, i formati pixel DXGI che non esempe il mapping alle strutture di formato pixel di Microsoft DirectDraw legacy e metadati aggiuntivi.

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

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Formato pixel della superficie (vedere [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Tipo: **[ **DIMENSIONE RISORSA \_ \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifica il tipo di risorsa. I valori seguenti per questo membro sono un subset dei valori nell'enumerazione [**D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) o [**D3D11 \_ RESOURCE \_ DIMENSION:**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension)



| Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                            | Valore |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ DIMENSION \_ TEXTURE1D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE1D) | La risorsa è una [trama 1D.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) Il **membro dwWidth** di [**DDS \_ HEADER**](dds-header.md) specifica le dimensioni della trama. In genere, si imposta il membro **dwHeight** di **DDS \_ HEADER** su 1. È inoltre necessario impostare il flag DDSD HEIGHT nel membro \_ **dwFlags** di **DDS \_ HEADER**.                      | 2     |
| DDS \_ DIMENSION \_ TEXTURE2D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D) | La risorsa è [una trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un'area specificata dai membri **dwWidth** e **dwHeight** di [**DDS \_ HEADER**](dds-header.md). È anche possibile usare questo tipo per identificare una trama mappa cubo. Per altre informazioni su come identificare una trama della mappa del cubo, vedere **membri miscFlag** **e arraySize.** | 3     |
| DDS \_ DIMENSION \_ TEXTURE3D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D) | La risorsa è una [trama 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un volume specificato dai membri **dwWidth**, **dwHeight** e **dwDepth** di [**DDS \_ HEADER**](dds-header.md). È anche necessario impostare il flag DDSD DEPTH nel membro \_ **dwFlags** di **DDS \_ HEADER**.                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifica altre opzioni meno comuni per le risorse. Il valore seguente per questo membro è un subset dei valori nell'enumerazione [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) o [**D3D11 \_ RESOURCE \_ MISC \_ FLAG:**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)



| Tipo                             | Descrizione                                                                                                  | Valore |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| RISORSA DDS \_ \_ MISC \_ TEXTURECUBE | Indica che una [trama 2D è](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) una trama mappa cubo. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi nella matrice.

Per una [trama 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) che è anche una trama mappa cubo, questo numero rappresenta il numero di cubi. Questo numero corrisponde al numero nel membro **NumCubes** di [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) o [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv). In questo caso, il file DDS contiene **trame 2D arraySize** \* 6. Per altre informazioni su questo caso, vedere la **descrizione di miscFlag.**

Per una [trama 3D,](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)è necessario impostare questo numero su 1.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Contiene metadati aggiuntivi (in precedenza era riservato). I 3 bit inferiori indicano la modalità alfa della risorsa associata. I 29 bit superiori sono riservati e sono in genere 0.



| Tipo                            | Descrizione                                                                                                                              | Valore |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| MODALITÀ ALFA DDS \_ \_ \_ SCONOSCIUTA       | Il contenuto del canale alfa è sconosciuto. Si tratta del valore per i file legacy, che in genere si presuppone sia alfa "diritto".                 | 0x0   |
| DDS \_ ALPHA \_ MODE \_ STRAIGHT      | Si presuppone che qualsiasi contenuto del canale alfa usi un valore alfa diritto.                                                                             | 0x1   |
| DDS \_ ALPHA \_ MODE \_ PREMULTIPLIED | Qualsiasi contenuto del canale alfa usa un valore alfa premoltilied. Gli unici formati di file legacy che indicano queste informazioni sono 'DX2' e 'DX4'. | 0x2   |
| DDS \_ ALPHA \_ MODE \_ OPAQUE        | Qualsiasi contenuto del canale alfa è impostato su completamente opaco.                                                                                    | 0x3   |
| MODALITÀ ALFA DDS \_ \_ \_ PERSONALIZZATA        | Qualsiasi contenuto del canale alfa viene usato come 4° canale e non deve rappresentare la trasparenza (diritto o premoltimullied).      | 0x4   |



 

> [!Note]  
> Le librerie di utilità D3DX 10 e [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) legacy non riusciranno a caricare . File DDS con **miscFlags2** diverso da zero.

 

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questa struttura insieme a [**un'intestazione \_ DDS**](dds-header.md) per archiviare una matrice di risorse in un file DDS. Per altre informazioni, vedere [Matrici di trame.](dx-graphics-dds-pguide.md)

Questa intestazione è presente se il **membro dwFourCC** della struttura [**\_ PIXELFORMAT DDS**](dds-pixelformat.md) è impostato su 'DX10'.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento per DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

