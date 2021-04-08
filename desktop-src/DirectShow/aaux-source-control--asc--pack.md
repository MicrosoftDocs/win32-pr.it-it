---
description: Pack del controllo del codice sorgente AAUX (ASC)
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: Pack del controllo del codice sorgente AAUX (ASC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747183"
---
# <a name="aaux-source-control-asc-pack"></a>Pack del controllo del codice sorgente AAUX (ASC)

Le tabelle seguenti elencano i valori usati dal driver MSDV per compilare il **dwDVAAuxCtl** e

membri **dwDVAAuxCtl1** della struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Per ulteriori informazioni, vedere [DVinfo Field Settings nel driver Msdv](dvinfo-field-settings-in-the-msdv-driver.md).

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

FINE REC (1)

1

1

1

1

MODALITÀ REC (3)

001

001

001

001

INSERISCI CH (3)

111

111

111

111

DRF (1)

1

1

1

1

VELOCITÀ (7)

010:0000

010:0000

010:0000

010:0000

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

ASC Pack (entrambi i blocchi audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

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

CGMS (2)

00

00

00

00

Riservato (4)

1111

1111

1111

1111

CEF (2)

00

00

00

00

REC ST (1)

1

1

1

1

FINE REC (1)

1

1

1

1

DISSOLVENZA ST (1)

1

1

1

1

FINE DISSOLVENZA (1)

1

1

1

1

Riservato (4)

1111

1111

1111

1111

DRF (1)

1

1

1

1

VELOCITÀ (7)

111:1000

110:0100

111:1000

110:0100

Riservato (8)

1111:1111

1111:1111

1111:1111

1111:1111

ASC Pack (entrambi i blocchi audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

\* La struttura *DVinfo* contiene due AAUX come Pack per i blocchi audio 1 e 2. DV50 ha quattro blocchi audio; i blocchi 3 e 4 non sono rappresentati nella struttura *DVinfo* .

Impostazioni DVCR 100 (pianificato)



Standard DV

DVCPRO 100-pianificato

FOURCC

dvh1

Sistema

1080-60i

720-60p

1080-50i

CGMS (2)

00

00

00

Riservato (4)

1111

1111

1111

CEF (2)

00

00

00

REC ST (1)

1

1

1

FINE REC (1)

1

1

1

DISSOLVENZA ST (1)

1

1

1

FINE DISSOLVENZA (1)

1

1

1

Riservato (4)

1111

1111

1111

DRF (1)

1

1

1

VELOCITÀ (7)

111:1000

111:1000

110:0100

Riservato (8)

1111:1111

1111:1111

1111:1111

ASC Pack (entrambi i blocchi audio)\*

0xFFF8FF3C

0xFFF8FF3C

0xFFE4FF3C



 

\* DVCPRO 100 include 8 blocchi audio; i blocchi da 3 a 8 non sono rappresentati nella struttura *DVinfo* .

## <a name="remarks"></a>Commenti

I codici di campo seguenti sono di particolare interesse:

-   **CGMS**: sistema di gestione della generazione della copia. 0 = copia consentita senza restrizioni.

    I Pack ASC effettivi nel flusso DV possono contenere valori diversi.

<!-- -->

-   **Modalità REC**: modalità di registrazione. 1 = originale
-   **Velocità**: velocità di riproduzione del VTR.

    Definizione IEC 61834:

    -   010:0000 = velocità normale, 525-60 o 625-50

    Definizione 314M SMPTE:

    -   111:1000 = velocità normale, 525-60
    -   110:0100 = velocità normale, 625-50

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Impostazioni dei campi DVINFO nel driver MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



