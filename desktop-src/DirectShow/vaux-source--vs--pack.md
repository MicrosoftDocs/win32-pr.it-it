---
description: Pacchetto di origine (VS) VAUX
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Pacchetto di origine (VS) VAUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f7ad2a91f1be1291b564013041e6dfa23bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314375"
---
# <a name="vaux-source-vs-pack"></a>Pacchetto di origine (VS) VAUX

Le tabelle seguenti elencano i valori usati dal driver MSDV per compilare il membro **dwDVVAuxSrc** della struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Per ulteriori informazioni, vedere [DVinfo Field Settings nel driver Msdv](dvinfo-field-settings-in-the-msdv-driver.md).

**Impostazioni DVCR**



Standard DV

DVCR (IEC 61834)

FOURCC

dvsl

DVSD

Sistema

525-60

625-50

525-60

625-50

CANALE TV (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

CANALE TV (4)

1111

1111

1111

1111

CODICE SORGENTE (2)

11

11

11

11

50/60 (1)

0

1

0

1

SPREVISTA (5)

0:0001

0:0001

0:0000

0:0000

CATEGORIA TUNER (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**Impostazioni DVCPRO 25 e DVCPRO 50 (pianificato)**



Standard DV

DVCPRO (SMPTE 314M)-pianificato

FOURCC

DV25

DV50

Sistema

525-60

625-50

525-60

625-50

Riservato (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

Riservato (4)

1111

1111

1111

1111

Riservato (2)

11

11

11

11

50/60 (1)

0

1

0

1

SPREVISTA (5)

0:0000

0:0000

0:0100

0:0100

VISC (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**Impostazioni DVCR 100 (pianificato)**



Standard DV

DVCPRO 100-pianificato

FOURCC

dvh1

Sistema

1080-60i

720-60p

1080-50i

Riservato (8)

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

EN (1)

1

1

1

CLF (2)

11

11

11

Riservato (4)

1111

1111

1111

Riservato (2)

11

11

11

50/60 (1)

0

0

1

SPREVISTA (5)

1:0100

1:1000

1:0100

VISC (8)

1111:1111

1111:1111

1111:1111

VS Pack

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>Commenti

I codici di campo seguenti sono di particolare interesse:

-   **B/W**: Flag nero e bianco. 1 = colore.
-   **50/60**: numero di campi.
    -   0 = campi di 60
    -   1 = 50 campi
-   **SPrevista**: tipo di segnale.

    Definizione IEC 61834:

    -   0:0000 = 525-60 o 625-50, DVSD
    -   0:0001 = 525-60 o 625-50, dvsl (come definito in IEC 61883-5)

    Definizione 314M SMPTE:

    -   0:0000 = compressione 4:1:1
    -   0:0100 = compressione 4:2:2

    Definizione di SMPTE 370:

    -   1:0100 = 1080/60i (60 Hz) o 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Impostazioni dei campi DVINFO nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



