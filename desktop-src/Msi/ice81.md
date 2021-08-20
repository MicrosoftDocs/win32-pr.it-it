---
description: ICE81 convalida la tabella MsiDigitalCertificate, la tabella MsiDigitalSignature, la tabella MsiPatchCertificate e la tabella MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bcf3228282339acd76ae4f20638cc24aeddf5279212b91aca0ece2b21867d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580811"
---
# <a name="ice81"></a>ICE81

ICE81 convalida la tabella [MsiDigitalCertificate](msidigitalcertificate-table.md), la [tabella MsiDigitalSignature](msidigitalsignature-table.md), la tabella [MsiPatchCertificate](msipatchcertificate-table.md)e [la tabella MsiPackageCertificate](msipackagecertificate-table.md). Questa azione personalizzata ICE pubblica avvisi per i certificati digitali non usati o senza riferimenti e invia un errore quando l'oggetto firmato non esiste o quando l'archivio dell'oggetto firmato non punta a dati esterni.

Si noti che ICE03 verifica che la voce nella colonna Tabella della tabella MsiDigitalSignature sia "Media".

## <a name="result"></a>Risultato

ICE81 pubblica gli avvisi seguenti per i certificati digitali inutilizzati o non referenziati.



| Avviso ICE81                                                                                                                                                      | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| Non è stato trovato alcun riferimento ai record nella tabella MsiDigitalCertificate nelle tabelle MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate. | Questo avviso viene restituito se tutti i record non sono usati.                |
| Non è stato trovato alcun riferimento al certificato digitale 1 nelle tabelle \[ \] MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.                         | Questo avviso viene restituito se alcuni record, ma non tutti, sono inutilizzati. |



 

ICE81 pubblica gli errori seguenti.



| Errore ICE81                                                                                                                                                              | Descrizione                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabella supporti inesistente. Di conseguenza, tutte le voci in MsiDigitalSignature non sono corrette                                                                                   | L'oggetto firmato non esiste. Questo errore viene restituito se la tabella Media non esiste ma MsiDigitalSignature contiene voci.                                |
| Oggetto firmato \[ mancante 2 \] in Media Table                                                                                                                               | L'oggetto \[ firmato 2 \] non esiste. Questo errore viene restituito se la tabella Media esiste, ma questa voce in MsiDigitalSignature non è presente nella tabella Media. |
| La voce nella tabella \[ 1 \] con la chiave \[ 2 è \] firmata. Di conseguenza, l'archivio deve puntare a un oggetto all'esterno del pacchetto (il valore di CABINET NON deve essere preceduto da \# ) | Il file CAB dell'oggetto firmato non punta a dati esterni. \[1 \] è il nome della tabella. \[2 \] è la chiave nella tabella Media.                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



