---
description: Pacchetto di origine (AS) AAUX
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Pacchetto di origine (AS) AAUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe479a0740da08f42ca5d80e1f0b6f5174f6917b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225477"
---
# <a name="aaux-source-as-pack"></a>Pacchetto di origine (AS) AAUX

Nelle tabelle seguenti sono elencati i valori usati dal driver MSDV per compilare i membri **dwDVAAuxSrc** e **DwDVAAuxSrc1** della struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Per ulteriori informazioni, vedere [DVinfo Field Settings nel driver Msdv](dvinfo-field-settings-in-the-msdv-driver.md).

Impostazioni DVCR



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

SPREVISTA (5)

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

COME Pack

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



 

Impostazioni DVCR 25 e DVCPRO 50 (pianificato)



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

DIMENSIONI AF (6)

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

SPREVISTA (5)

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

COME Pack

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
> \* La struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) contiene due AAUX come Pack per i blocchi audio 1 e 2. DV50 ha quattro blocchi audio; i blocchi 3 e 4 non sono rappresentati nella struttura **DVinfo** .

 

Impostazioni DVCR 100 (pianificato)



Standard DV

DVCPRO 100-pianificato

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

DIMENSIONI AF (6)

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

SPREVISTA (5)

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

COME Pack

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \* DVCPRO 100 include 8 blocchi audio; i blocchi da 3 a 8 non sono rappresentati nella struttura [DVinfo](dvinfo-field-settings-in-the-msdv-driver.md) .

 

## <a name="remarks"></a>Commenti

I codici di campo seguenti sono di particolare interesse:

-   LF: flag della modalità bloccata. Indica se l'audio è bloccato.
    -   0 = bloccato
    -   1 = sbloccato
-   DIMENSIONI AF: dimensioni del frame audio. Specifica il numero di campioni audio per fotogramma.

    Definizione IEC 61834:

    -   00:1111 = 1068 campioni per frame
    -   01:0000 = 1280 campioni per frame

    Definizione 314M SMPTE:

    -   01:0110 = 1602 campioni per frame
    -   01:1000 = 1920 campioni per frame

    A seconda della frequenza dei fotogrammi, il numero esatto di campioni in un frame potrebbe variare. Ad esempio, NTSC è 30000/1001 frame al secondo (29,97 fps). Con audio 32-kHz sono disponibili circa 1067,73 esempi audio per frame. Quindi, la velocità nominale è 1068, ma il numero effettivo varia in base al frame. Inoltre, con l'audio sbloccato, il numero di campioni audio per frame può variare entro un determinato intervallo nel tempo.

<!-- -->

-   SM: modalità stereo.
    -   0 = stereo
    -   1 = mono
-   CHN: numero di canali audio per blocco audio.
    -   0 = un canale per ogni blocco audio
    -   1 = due canali per blocco audio
-   MODALITÀ AUDIO: indica il contenuto del segnale audio su ogni canale. L'interpretazione di questo campo dipende dai valori inseriti nei campi SM e CHN. Le definizioni indicate di seguito sono relative ai valori utilizzati da MSDV; Per ulteriori informazioni, vedere le specifiche.

    Definizione IEC 61834:

    -   0000 = ch a/c/e/g è il canale sinistro, ch b/d/f/h è il canale corretto
    -   1111 = nessun dato audio

    Definizione 314M SMPTE:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: numero di campi.
    -   0 = campi di 60
    -   1 = 50 campi
-   SPREVISTA: tipo di sistema.

    Definizione IEC 61834:

    -   00000 = 525-60 o 625-50, DVSD
    -   00001 = 525-60 o 625-50, dvsl (vedere IEC 61883-5)

    Definizione di SMPTE 314M/SPMTE 370:

    -   00000 = 2 blocchi audio per ogni fotogramma video
    -   00010 = 4 blocchi audio per ogni fotogramma video
    -   00011 = 8 blocchi audio per ogni fotogramma video

-   SMP: frequenza di campionamento.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU: quantizzazione.
    -   0 = 16 bit lineari
    -   1 = 12 bit non lineari

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Impostazioni dei campi DVINFO nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



