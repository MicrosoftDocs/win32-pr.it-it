---
description: Pacchetto AAUX Source (AS)
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Pacchetto AAUX Source (AS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a2d8aa11c9560b2aa59165afd9bdaae775be7755a7a7d2a5e87a80df412d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160262"
---
# <a name="aaux-source-as-pack"></a>Pacchetto AAUX Source (AS)

Le tabelle seguenti elencano i valori usati dal driver MSDV per compilare i membri **dwDVAAuxSrc** e **dwDVAAuxSrc1** della struttura [**DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Per altre informazioni, vedere [DVINFO Field Impostazioni nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

DVCR Impostazioni



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

LF (1)

1

1

1

1

Riservato (1)

1

1

1

1

DIMENSIONI AF (6)

00:1111

01:0000

00:1111

01:0000

SM (1)

0

0

0

0

CHN (2)

01

01

01

01

PA (1)

1

1

1

1

MODALITÀ AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0000

0000

1111

1111

Riservato (1)

1

1

1

1

ML (1)

1

1

1

1

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

EF (1)

1

1

1

1

TC (1)

1

1

1

1

SMP (3)

010

010

010

010

QU (3)

001

001

001

001

PACCHETTO AS

    Audio Block 1\*

0xD1C130CF

0xD1E130D0

0xD1C030CF

0xD1E030D0

    Audio Block 2\*

0x00000000

0x00000000

0xD1C03FCF

0xD1E03FD0



 

DVCR 25 e DVCPRO 50 Impostazioni (pianificato)



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

LF (1)

0

0

0

0

Riservato (1)

1

1

1

1

AF SIZE (6)

01:0110

01:1000

01:0110

01:1000

Riservato (1)

0

0

0

0

CHN (2)

00

00

00

00

Riservato (1)

1

1

1

1

MODALITÀ AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

0001

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

0:0010

0:0010

Riservato (2)

11

11

11

11

SMP (3)

7000

7000

7000

7000

QU (3)

7000

7000

7000

7000

AS Pack

    Audio Block 1\*

0xC0C01056

0xC0E01058

0xC0C21056

0xC0E21058

    Audio Block 2\*

0xC0C01156

0xC0E01158

0xC0C21156

0xC0E21158



 

> [!Note]  
> \* La [**struttura DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) contiene due pacchetti AAUX AS, per i blocchi audio 1 e 2. DV50 ha quattro blocchi audio. I blocchi 3 e 4 non sono rappresentati nella **struttura DVINFO.**

 

DVCR 100 Impostazioni (pianificato)



DV Standard

DVCPRO 100 - Pianificato

FOURCC

dvh1

Sistema

1080-60i

720-60p

1080-50i

LF (1)

0

0

0

Riservato (1)

1

1

1

AF SIZE (6)

01:0110

01:0110

01:1000

Riservato (1)

0

0

0

CHN (2)

00

00

00

Riservato (1)

1

1

1

MODALITÀ AUDIO (4)

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

Riservato (2)

11

11

11

50/60 (1)

0

0

1

STYPE (5)

0:0011

0:0011

0:0011

Riservato (2)

11

11

11

SMP (3)

7000

7000

7000

QU (3)

7000

7000

7000

AS Pack

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \*DVCPRO 100 ha 8 blocchi audio; I blocchi da 3 a 8 non sono rappresentati nella [struttura DVINFO.](dvinfo-field-settings-in-the-msdv-driver.md)

 

## <a name="remarks"></a>Commenti

I codici di campo seguenti sono di interesse:

-   LF: flag della modalità bloccata. Indica se l'audio è bloccato.
    -   0 = Bloccato
    -   1 = Sbloccato
-   DIMENSIONI AF: dimensioni del fotogramma audio. Specifica il numero di campioni audio per fotogramma.

    Definizione IEC 61834:

    -   00:1111 = 1068 campioni per fotogramma
    -   01:0000 = 1280 campioni per fotogramma

    Definizione SMPTE 314M:

    -   01:0110 = 1602 campioni per fotogramma
    -   01:1000 = 1920 campioni per fotogramma

    A seconda della frequenza dei fotogrammi, il numero esatto di campioni in un frame può variare. Ad esempio, NTSC è 30000/1001 fotogrammi al secondo (29,97 fps). Con audio a 32 kHz, sono disponibili circa 1067,73 campioni audio per fotogramma. Il tasso nominale è quindi 1068, ma il numero effettivo varia per fotogramma. Inoltre, con l'audio sbloccato, il numero di campioni audio per fotogramma può variare all'interno di un determinato intervallo nel tempo.

<!-- -->

-   SM: modalità stereo.
    -   0 = Stereo
    -   1 = Mono
-   CHN: numero di canali audio per blocco audio.
    -   0 = Un canale per blocco audio
    -   1 = Due canali per blocco audio
-   MODALITÀ AUDIO: indica il contenuto del segnale audio in ogni canale. L'interpretazione di questo campo dipende dai valori inseriti nei campi SM e CHN. Le definizioni riportate di seguito sono relative ai valori usati da MSDV. Per altre informazioni, vedere le specifiche.

    Definizione IEC 61834:

    -   0000 = Ch a/c/e/g è il canale sinistro, Ch b/d/f/h è il canale destro
    -   1111 = nessun dato audio

    Definizione SMPTE 314M:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: numero di campi.
    -   0 = 60 campi
    -   1 = 50 campi
-   STYPE: tipo di sistema.

    Definizione IEC 61834:

    -   00000 = 525-60 o 625-50, dvsd
    -   00001 = 525-60 o 625-50, dvsl (vedere IEC 61883-5)

    Definizione SMPTE 314M/SPMTE 370:

    -   00000 = 2 blocchi audio per fotogramma video
    -   00010 = 4 blocchi audio per fotogramma video
    -   00011 = 8 blocchi audio per fotogramma video

-   SMP: frequenza di campionamento.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU: quantizzazione.
    -   0 = lineare a 16 bit
    -   1 = 12 bit non lineari

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campi DVINFO Impostazioni nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



