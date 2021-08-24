---
title: DDS_HEADER struttura (Dds.h)
description: Descrive un'intestazione di file DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER struttura DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d974c319206d0a0cbe6abda291e9d376bd6478a5b8eb8ba3ef3bb12f182b1288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746001"
---
# <a name="dds_header-structure"></a>Struttura DDS \_ HEADER

Descrive un'intestazione di file DDS.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dimensione della struttura . Questo membro deve essere impostato su 124.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flag per indicare quali membri contengono dati validi.



| Flag              | Descrizione                                                  | Valore    |
|-------------------|--------------------------------------------------------------|----------|
| DDSD \_ CAPS        | Obbligatorio in ogni file con estensione dds.                                 | 0x1      |
| ALTEZZA \_ DDSD      | Obbligatorio in ogni file con estensione dds.                                 | 0x2      |
| LARGHEZZA \_ DDSD       | Obbligatorio in ogni file con estensione dds.                                 | 0x4      |
| PASSO \_ DDSD       | Obbligatorio quando viene specificata l'altezza per una trama non compressa. | 0x8      |
| DDSD \_ PIXELFORMAT | Obbligatorio in ogni file con estensione dds.                                 | 0x1000   |
| DDSD \_ MIPMAPCOUNT | Obbligatorio in una trama mipmapped.                             | 0x20000  |
| DDSD \_ LINEARSIZE  | Obbligatorio quando viene specificato un passo per una trama compressa.    | 0x80000  |
| PROFONDITÀ \_ DDSD       | Obbligatorio in una trama di profondità.                                 | 0x800000 |



 

> [!Note]  
> Quando si scrivono file DDS, è necessario impostare i flag DDSD CAPS e DDSD PIXELFORMAT e, per le trame mipmapped, è necessario impostare anche il \_ \_ flag \_ MIPMAPCOUNT DDSD. Tuttavia, quando si legge un file DDS, non è consigliabile basarsi sui flag DDSD \_ CAPS, DDSD PIXELFORMAT e \_ DDSD MIPMAPCOUNT impostati perché alcuni writer di tale file potrebbero non impostare questi \_ flag.

 

Il flag TEXTURE DDS HEADER FLAGS, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag \_ DDSD \_ CAPS, DDSD \_ HEIGHT, DDSD WIDTH e \_ \_ DDSD PIXELFORMAT.

Il \_ flag MIPMAP DDS HEADER FLAGS, definito in Dds.h, è uguale al \_ flag \_ \_ MIPMAPCOUNT DDSD.

Il flag VOLUME DDS HEADER FLAGS, definito \_ \_ in \_ Dds.h, è uguale al flag DDSD \_ DEPTH.

Il \_ flag PITCH DDS HEADER FLAGS, definito in \_ \_ Dds.h, è uguale al flag PITCH \_ DDSD.

Il flag DDS HEADER FLAGS LINEARSIZE, definito in Dds.h, è uguale al \_ \_ flag \_ DDSD \_ LINEARSIZE.

</dd> <dt>

**dwHeight**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Altezza della superficie (in pixel).

</dd> <dt>

**dwWidth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Larghezza della superficie (in pixel).

</dd> <dt>

**dwPitchOrLinearSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Passo o numero di byte per riga di analisi in una trama non compressa. numero totale di byte nella trama di primo livello per una trama compressa. Per informazioni su come calcolare l'altezza, vedere la sezione Layout di file DDS della [Guida per programmatori per DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwDepth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondità di una trama del volume (in pixel), in caso contrario non utilizzata.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di livelli mipmap, altrimenti inutilizzati.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Non utilizzato.

</dd> <dt>

**ddspf**
</dt> <dd>

Tipo: **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**

</dd> <dd>

Formato pixel (vedere [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).

</dd> <dt>

**dwCaps**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Specifica la complessità delle superfici archiviate.



| Flag             | Descrizione                                                                                                                              | Valore    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| COMPLESSO DDSCAPS \_ | Facoltativo. deve essere usato in qualsiasi file che contiene più di una superficie (una mappa mipmap, una mappa dell'ambiente cubico o una trama di volume mipmapped). | 0x8      |
| DDSCAPS \_ MIPMAP  | Facoltativo. deve essere usato per un mipmap.                                                                                                   | 0x400000 |
| TRAMA DDSCAPS \_ | Necessario                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Quando si scrivono file con estensione dds, è necessario impostare il flag TEXTURE DDSCAPS e per più superfici è necessario impostare anche il \_ flag COMPLEX DDSCAPS. \_ Tuttavia, quando si legge un file con estensione dds, non è consigliabile basarsi sui flag DDSCAPS TEXTURE e DDSCAPS COMPLEX impostati perché alcuni writer di tale file potrebbero non impostare questi \_ \_ flag.

 

Il flag MIPMAP DDS SURFACE FLAGS, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag \_ DDSCAPS COMPLEX e \_ DDSCAPS \_ MIPMAP.

Il flag TEXTURE DDS SURFACE FLAGS, definito \_ \_ in \_ Dds.h, è uguale al flag TEXTURE DDSCAPS. \_

Il \_ flag \_ CUBEMAP DDS SURFACE FLAGS, definito in \_ Dds.h, è uguale al flag COMPLEX DDSCAPS. \_

</dd> <dt>

**dwCaps2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Dettagli aggiuntivi sulle superfici archiviate.



| Flag                         | Descrizione                                            | Valore    |
|------------------------------|--------------------------------------------------------|----------|
| MAPPING DEI CUBI DDSCAPS2 \_            | Obbligatorio per una mappa del cubo.                               | 0x200    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEX | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x400    |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x800    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEY | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x1000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEY | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x2000   |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x4000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x8000   |
| DDSCAPS2 \_ VOLUME             | Obbligatorio per una trama del volume.                         | 0x200000 |



 

Il flag DDS CUBEMAP POSITIVEX, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag CUBEMAP DDSCAPS2 e \_ DDSCAPS2 \_ CUBEMAP \_ POSITIVEX.

Il flag DDS CUBEMAP NEGATIVEX, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag DDSCAPS2 CUBEMAP e \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX.

Il flag DDS CUBEMAP POSITIVEY, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag CUBEMAP DDSCAPS2 e \_ DDSCAPS2 \_ CUBEMAP \_ POSITIVEY.

Il flag DDS CUBEMAP NEGATIVEY, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag CUBEMAP DDSCAPS2 e \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEY.

Il flag DDS CUBEMAP POSITIVEZ, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag CUBEMAP DDSCAPS2 e \_ DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ.

Il flag DDS CUBEMAP NEGATIVEZ, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag CUBEMAP DDSCAPS2 e \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ.

Il flag DDS CUBEMAP ALLFACES, definito in Dds.h, è una combinazione OR bit per bit dei \_ \_ flag DDS \_ \_ CUBEMAP POSITIVEX, DDS \_ CUBEMAP \_ NEGATIVEX, DDS \_ CUBEMAP \_ POSITIVEY, DDS \_ CUBEMAP \_ NEGATIVEY, DDS \_ CUBEMAP POSITIVEZ e \_ DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ.

Il flag VOLUME DDS FLAGS, definito \_ \_ in Dds.h, è uguale al flag VOLUME DDSCAPS2. \_

> [!Note]  
> Anche se Direct3D 9 supporta mappe cubi parziali, Direct3D 10, 10.1 e 11 richiedono la definizione di tutte e sei le visi della mappa cubo, ovvero è necessario impostare \_ CUBEMAP \_ ALLFACES DDS.

 

</dd> <dt>

**dwCaps3**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Non utilizzato.

</dd> <dt>

**dwCaps4**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Non utilizzato.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Non utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Includere flag in **dwFlags** per i membri della struttura che contengono dati validi.

Usare questa struttura in combinazione con [**un'intestazione \_ \_ DDS DXT10**](dds-header-dxt10.md) per archiviare una matrice di risorse in un file DDS. Per altre informazioni, vedere [Matrici di trame.](dx-graphics-dds-pguide.md)

**DDS \_ HEADER** è identica alla struttura DDSURFACEDESC2 di DirectDraw senza dipendenze DirectDraw.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento per DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

