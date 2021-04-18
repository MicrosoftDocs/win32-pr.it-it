---
title: Struttura DDS_HEADER (DDS. h)
description: Descrive un'intestazione del file DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- Struttura DDS_HEADER DDS
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
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322292"
---
# <a name="dds_header-structure"></a>\_Struttura dell'intestazione DDS

Descrive un'intestazione del file DDS.

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

Dimensione della struttura. Questo membro deve essere impostato su 124.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flag per indicare quali membri contengono dati validi.



| Flag              | Descrizione                                                  | Valore    |
|-------------------|--------------------------------------------------------------|----------|
| DDSD \_ Caps        | Obbligatorio in ogni file. DDS.                                 | 0x1      |
| \_altezza DDSD      | Obbligatorio in ogni file. DDS.                                 | 0x2      |
| \_larghezza DDSD       | Obbligatorio in ogni file. DDS.                                 | 0x4      |
| DDSD \_ pitch       | Obbligatorio quando viene fornito un pitch per una trama non compressa. | 0x8      |
| DDSD \_ PIXELFORMAT | Obbligatorio in ogni file. DDS.                                 | 0x1000   |
| \_MIPMAPCOUNT DDSD | Obbligatorio in una trama mipmap.                             | 0x20000  |
| \_LINEARSIZE DDSD  | Obbligatorio quando viene fornito un pitch per una trama compressa.    | 0x80000  |
| \_profondità DDSD       | Obbligatorio in una trama di profondità.                                 | 0x800000 |



 

> [!Note]  
> Quando si scrivono file con estensione DDS, è necessario impostare i \_ flag DDSD Caps e DDSD \_ PIXELFORMAT e per le trame mipmap è necessario impostare anche il \_ flag DDSD MIPMAPCOUNT. Tuttavia, quando si legge un file con estensione DDS, è consigliabile non basarsi sui \_ flag DDSD Caps, DDSD \_ PIXELFORMAT e DDSD \_ MIPMAPCOUNT impostati in quanto alcuni writer di tale file potrebbero non impostare questi flag.

 

Il \_ \_ flag di trama dei flag di intestazione DDS \_ , definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDSD Caps, DDSD \_ Height, DDSD \_ Width e DDSD \_ PIXELFORMAT.

Il flag di \_ intestazione DDS \_ flag \_ MIPMAP, che è definito in DDS. h, è uguale al \_ flag DDSD MIPMAPCOUNT.

Il flag \_ del \_ volume dei flag di intestazione DDS \_ , definito in DDS. h, è uguale al \_ flag di profondità DDSD.

Il flag \_ di \_ pitch dei flag di intestazione DDS \_ , definito in DDS. h, è uguale al \_ flag di pitch DDSD.

Il flag di \_ intestazione DDS \_ flag \_ LINEARSIZE, che è definito in DDS. h, è uguale al \_ flag DDSD LINEARSIZE.

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

Il pitch o il numero di byte per riga di analisi in una trama non compressa; numero totale di byte nella trama di primo livello per una trama compressa. Per informazioni su come calcolare il passo, vedere la sezione relativa al layout dei file DDS della [Guida alla programmazione per DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwDepth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondità di una trama del volume (in pixel), altrimenti inutilizzata.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di livelli di mipmap, altrimenti non utilizzati.

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
| \_complesso DDSCAPS | Opzionale deve essere usato in qualsiasi file che contiene più di una superficie (un mipmap, una mappa dell'ambiente cubica o una trama del volume mipmap). | 0x8      |
| \_MIPMAP DDSCAPS  | Opzionale deve essere usato per un mipmap.                                                                                                   | 0x400000 |
| \_trama DDSCAPS | Necessario                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Quando si scrivono file con estensione DDS, è necessario impostare il \_ flag di trama ddsCaps e per più superfici è necessario impostare anche il \_ flag complesso ddsCaps. Tuttavia, quando si legge un file con estensione DDS, è consigliabile non basarsi sulla \_ trama ddsCaps e sui \_ flag complessi ddsCaps impostati, perché alcuni writer di tale file potrebbero non impostare questi flag.

 

Il \_ flag MIPMAP della superficie DDS \_ \_ , definito in DDS. h, è una combinazione OR bit per bit dei \_ flag ddsCaps Complex e ddsCaps \_ MIPMAP.

Il flag \_ di \_ trama dei flag di superficie DDS \_ , definito in DDS. h, è uguale al \_ flag di trama ddsCaps.

Il flag \_ mappa cubi della superficie DDS \_ \_ , definito in DDS. h, equivale al \_ flag ddsCaps complesso.

</dd> <dt>

**dwCaps2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ulteriori dettagli sulle superfici archiviate.



| Flag                         | Descrizione                                            | Valore    |
|------------------------------|--------------------------------------------------------|----------|
| \_Mappa cubi DDSCAPS2            | Obbligatorio per una mappa cubo.                               | 0x200    |
| DDSCAPS2 \_ mappa cubi \_ POSITIVEX | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x400    |
| DDSCAPS2 \_ mappa cubi \_ NEGATIVEX | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x800    |
| DDSCAPS2 \_ mappa cubi \_ positivo | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x1000   |
| DDSCAPS2 \_ mappa cubi \_ negativo | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x2000   |
| DDSCAPS2 \_ mappa cubi \_ POSITIVEZ | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x4000   |
| DDSCAPS2 \_ mappa cubi \_ NEGATIVEZ | Obbligatorio quando queste superfici vengono archiviate in una mappa cubo. | 0x8000   |
| \_Volume DDSCAPS2             | Obbligatorio per una trama del volume.                         | 0x200000 |



 

Il \_ flag DDS mappa cubi \_ POSITIVEX, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi POSITIVEX \_ .

Il \_ flag DDS mappa cubi \_ NEGATIVEX, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi NEGATIVEX \_ .

Il \_ \_ flag positivo mappa cubi DDS, definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi \_ positivo.

Il \_ flag mappa cubi \_ , che è definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi \_ negative.

Il \_ flag DDS mappa cubi \_ POSITIVEZ, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi POSITIVEZ \_ .

Il \_ flag DDS mappa cubi \_ NEGATIVEZ, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi NEGATIVEZ \_ .

Il \_ flag DDS mappa cubi \_ ALLFACES, definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDS mappa cubi \_ POSITIVEX, DDS \_ mappa cubi \_ NEGATIVEX, DDS \_ mappa cubi \_ positivey, DDS \_ mappa cubi \_ negative, DDS \_ mappa cubi \_ POSITIVEZ e \_ \_ DDSCAPS2 mappa cubi NEGATIVEZ.

Il flag del \_ volume dei flag DDS \_ , definito in DDS. h, è uguale al flag del \_ volume DDSCAPS2.

> [!Note]  
> Sebbene Direct3D 9 supporti le mappe di cubi parziali, Direct3D 10, 10,1 e 11 richiedono la definizione di tutti e sei i visi della mappa cubo, ovvero è necessario impostare DDS \_ mappa cubi \_ ALLFACES.

 

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

Includere i flag in **dwFlags** per i membri della struttura che contengono dati validi.

Usare questa struttura insieme a un' [**intestazione DDS \_ \_ DXT10**](dds-header-dxt10.md) per archiviare una matrice di risorse in un file DDS. Per altre informazioni, vedere [matrici di trame](dx-graphics-dds-pguide.md).

**DDS \_ L'intestazione** è identica alla struttura DDSURFACEDESC2 di DirectDraw senza dipendenze di DirectDraw.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento per DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

