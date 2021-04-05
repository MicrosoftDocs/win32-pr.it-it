---
description: ICE81 convalida la tabella MsiDigitalCertificate, la tabella MsiDigitalSignature, la tabella MsiPatchCertificate e la tabella MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752791"
---
# <a name="ice81"></a>ICE81

ICE81 convalida la tabella [MsiDigitalCertificate](msidigitalcertificate-table.md), la tabella [MsiDigitalSignature](msidigitalsignature-table.md), la tabella [MsiPatchCertificate](msipatchcertificate-table.md)e la [tabella MsiPackageCertificate](msipackagecertificate-table.md). Questa azione personalizzata del ghiaccio invia avvisi per i certificati digitali non usati o senza riferimenti e invia un errore quando l'oggetto firmato non esiste o quando il cabinet dell'oggetto firmato non punta a dati esterni.

Si noti che ICE03 verifica che la voce nella colonna della tabella nella tabella MsiDigitalSignature sia "media".

## <a name="result"></a>Risultato

ICE81 invia gli avvisi seguenti per i certificati digitali non usati o senza riferimenti.



| Avviso di ICE81                                                                                                                                                      | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Nessun riferimento a nessuno dei record nella tabella MsiDigitalCertificate è stato trovato nelle tabelle MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate. | Questo avviso viene restituito se tutti i record non vengono usati.                |
| Nessun riferimento al certificato digitale \[ 1 \] è stato trovato nelle tabelle MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.                         | Questo avviso viene restituito se alcuni record, ma non tutti, non sono utilizzati. |



 

ICE81 invia i seguenti errori.



| Errore ICE81                                                                                                                                                              | Descrizione                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La tabella supporti non esiste. Di conseguenza, tutte le voci in MsiDigitalSignature non sono corrette                                                                                   | L'oggetto firmato non esiste. Questo errore viene restituito se la tabella dei supporti non esiste ma MsiDigitalSignature contiene voci.                                |
| Oggetto firmato mancante \[ 2 \] nella tabella supporti                                                                                                                               | L'oggetto firmato \[ 2 non \] esiste. Questo errore viene restituito se la tabella supporti esiste, ma questa voce in MsiDigitalSignature non è presente nella tabella dei supporti. |
| La voce nella tabella \[ 1 \] con chiave \[ 2 \] è firmata. Il cabinet deve quindi puntare a un oggetto all'esterno del pacchetto (il valore del file CAB non deve essere preceduto da \# ) | Il cabinet dell'oggetto firmato non punta a dati esterni. \[1 \] è il nome della tabella. \[2 \] è la chiave nella tabella dei supporti.                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



