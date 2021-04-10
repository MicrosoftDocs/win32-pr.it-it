---
description: Pack del controllo del codice sorgente (VSC) di VAUX
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Pack del controllo del codice sorgente (VSC) di VAUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed51363a15c0024dcaf3edca5d21217cb29396d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883089"
---
# <a name="vaux-source-control-vsc-pack"></a>Pack del controllo del codice sorgente (VSC) di VAUX

Le tabelle seguenti elencano i valori usati dal driver MSDV per compilare il membro **dwDVVAuxCtl** della struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Per ulteriori informazioni, vedere [DVinfo Field Settings nel driver Msdv](dvinfo-field-settings-in-the-msdv-driver.md).

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

GENERE (7)

111:1111

111:1111

111:1111

111:1111

VSC Pack

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

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



 

**Impostazioni DVCPRO 100 (pianificato)**



Standard DV

DVCPRO 100-pianificato

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

I codici di campo seguenti sono di particolare interesse:

-   **CGMS**: sistema di gestione della generazione della copia. 0 = copia consentita senza restrizioni.

    I pacchetti VSC effettivi nel flusso DV possono contenere valori diversi.

<!-- -->

-   **Modalità REC**: modalità di registrazione. 1 = originale.
-   **Disp**: Visualizza la modalità di selezione. 000 = 4:3 proporzioni, formato completo; 010 = 16:9 proporzioni.
-   **BCSYS**: sistema broadcast. Questo campo definisce il tipo di informazioni di segnalazione schermo intero.
    -   0 = tipo 0 (vedere IEC 61880)
    -   1 = tipo 1 (vedere ETSI EN 300 294)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Impostazioni dei campi DVINFO nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



