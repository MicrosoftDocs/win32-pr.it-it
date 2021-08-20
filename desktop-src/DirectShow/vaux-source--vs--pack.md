---
description: PACCHETTO DI ORIGINE VAUX (VS)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: PACCHETTO DI ORIGINE VAUX (VS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477e7a3257c11d6d8b42e16d2f066251452bc42a489abe9e666e374a565fa77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072099"
---
# <a name="vaux-source-vs-pack"></a>PACCHETTO DI ORIGINE VAUX (VS)

Le tabelle seguenti elencano i valori usati dal driver MSDV per compilare il membro **dwDVVAuxSrc** della [**struttura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Per altre informazioni, vedere [DVINFO Field Impostazioni nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**DVCR Impostazioni**



DV Standard

DVCR (IEC 61834)

FOURCC

dvsl

dvsd

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

STYPE (5)

0:0001

0:0001

0:0000

0:0000

CATEGORIA DI SINER (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**DVCPRO 25 e DVCPRO 50 Impostazioni (pianificato)**



DV Standard

DVCPRO (SMPTE 314M) - Pianificato

FOURCC

dv25

dv50

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

STYPE (5)

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



 

**DVCR 100 Impostazioni (pianificato)**



DV Standard

DVCPRO 100 - Pianificato

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

STYPE (5)

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

I codici di campo seguenti sono di interesse:

-   **B/W:** flag bianco e nero. 1 = colore.
-   **50/60**: numero di campi.
    -   0 = 60 campi
    -   1 = 50 campi
-   **STYPE:** tipo di segnale.

    Definizione IEC 61834:

    -   0:0000 = 525-60 o 625-50, dvsd
    -   0:0001 = 525-60 o 625-50, dvsl (come definito in IEC 61883-5)

    Definizione SMPTE 314M:

    -   0:0000 = compressione 4:1:1
    -   0:0100 = compressione 4:2:2

    Definizione di SMPTE 370:

    -   1:0100 = 1080/60i (60 Hz) o 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campi DVINFO Impostazioni nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



