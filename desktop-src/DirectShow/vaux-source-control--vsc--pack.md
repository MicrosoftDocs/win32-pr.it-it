---
description: VAUX Source Control (VSC) Pack
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: VAUX Source Control (VSC) Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdc91d5c4b2cea460c85b696c59bfce7799d39aed0a6bfcbc03f3d3c522a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072075"
---
# <a name="vaux-source-control-vsc-pack"></a>VAUX Source Control (VSC) Pack

Nelle tabelle seguenti sono elencati i valori utilizzati dal driver MSDV per compilare il membro **dwDVVAuxCtl** della [**struttura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Per altre informazioni, vedere [DVINFO Field Impostazioni nel driver MSDV.](dvinfo-field-settings-in-the-msdv-driver.md)

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

CGMS (2)

00

00

00

00

ISR (2)

11

11

11

11

CMP (2)

11

11

11

11

SS (2)

11

11

11

11

REC ST (1)

1

1

1

1

Riservato (1)

1

1

1

1

MODALITÀ REC (2)

00

00

00

00

Riservato (1)

1

1

1

1

DISP (3)

7000

7000

7000

7000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

ST (1)

1

1

1

1

SC (1)

1

1

1

1

BCSYS (2)

00

01

00

01

Riservato (1)

1

1

1

1

GENRE (7)

111:1111

111:1111

111:1111

111:1111

VSC Pack

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

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

CGMS (2)

00

00

00

00

Riservato (6)

11:1111

11:1111

11:1111

11:1111

Riservato (2)

11

11

11

11

Riservato (2)

00

00

00

00

Riservato (1)

1

1

1

1

DISP (3)

7000

7000

7000

7000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

Riservato (2)

11

11

11

11

Riservato (2)

00

00

00

00

Riservato (8)

1111:1111

1111:1111

1111:1111

1111:1111

VSC Pack

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**DVCPRO 100 Impostazioni (pianificato)**



DV Standard

DVCPRO 100 - Pianificato

FOURCC

dvh1

Sistema

1080-60i

720p-60p

1080-50i

CGMS (2)

00

00

00

Riservato (6)

11:1111

11:1111

11:1111

Riservato (2)

11

11

11

Riservato (2)

00

00

00

Riservato (1)

1

1

1

DISP (3)

010

010

010

FF (1)

1

1

1

FS (1)

1

1

1

FC (1)

1

1

1

IL (1)

1

1

1

Riservato (2)

11

11

11

Riservato (2)

00

00

00

Riservato (8)

1111:1111

1111:1111

1111:1111

VSC Pack

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>Commenti

I codici di campo seguenti sono di interesse:

-   **CGMS:** sistema di gestione della generazione di copie. 0 = la copia è consentita senza restrizioni.

    I pacchetti VSC effettivi nel flusso DV possono contenere valori diversi.

<!-- -->

-   **REC MODE:** modalità di registrazione. 1 = Originale.
-   **DISP:** consente di visualizzare la modalità di selezione. 000 = proporzioni 4:3, formato completo; 010 = proporzioni 16:9.
-   **BCSYS:** sistema di trasmissione. Questo campo definisce il tipo di informazioni di segnalazione dello schermo wide.
    -   0 = tipo 0 (vedere IEC 61880)
    -   1 = tipo 1 (vedere ETSI EN 300 294)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campi DVINFO Impostazioni nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



