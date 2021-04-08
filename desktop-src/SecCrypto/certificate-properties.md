---
description: Servizi certificati supporta l'utilizzo di certificati come definito nella raccomandazione ITU-T X. 509 (anche ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Proprietà certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881006"
---
# <a name="certificate-properties"></a>Proprietà certificato

Servizi certificati supporta l'utilizzo di certificati come definito nella raccomandazione ITU-T [*X. 509*](../secgloss/x-gly.md) (anche ISO/IEC 9594-8). Di seguito sono riportate le proprietà contenute in un certificato X. 509 standard.



| Campo                                       | Descrizione                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione                                     | Numero di versione del formato del certificato.                                                                                                                                                                       |
| Numero di serie                               | Numero di serie del certificato. Questo numero viene assegnato dall'emittente ed è univoco all'interno dell'elenco dei certificati emessi dall'emittente.                                                                          |
| Identificatore e parametri dell'algoritmo         | Algoritmo di firma e qualsiasi parametro usato dall'emittente.                                                                                                                                                      |
| Issuer                                      | Nome dell' [*autorità di certificazione*](../secgloss/c-gly.md) che ha emesso il certificato.                                               |
| Non prima (Data)                           | Il certificato non è valido prima di questa data.                                                                                                                                                                         |
| Non dopo (Data)                            | Il certificato non è valido dopo questa data.                                                                                                                                                                          |
| Nome soggetto                                | Nome della persona o dell'entità a cui viene emesso il certificato. Questo campo può includere anche organizzazione del destinatario del certificato, unità organizzativa, località, stato o provincia e paese/area geografica. |
| Algoritmo e parametri della chiave pubblica dell'oggetto | Algoritmo e tutti i parametri utilizzati per la [*chiave pubblica*](../secgloss/p-gly.md)del soggetto.                                                                       |
| Chiave pubblica del soggetto                          | Chiave pubblica effettiva, ovvero una stringa di bit.                                                                                                                                                                           |
| Firma                                   | Firma fornita dall'emittente.                                                                                                                                                                            |



 

Un certificato può contenere gli elementi seguenti, a seconda della versione [*X. 509*](../secgloss/x-gly.md) del certificato.



| Campo facoltativo    | Descrizione                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID univoco dell'autorità di certificazione  | Utilizzato per rendere non ambiguo il nome dell'autorità emittente se è stato utilizzato da più di un'entità. Presente solo nelle versioni [*X. 509*](../secgloss/x-gly.md) 2,0 o successive.<br/> |
| ID oggetto univoco | Utilizzato per rendere ambiguo il nome del soggetto se è stato utilizzato da più di un'entità. Presente solo in X. 509 2,0 o versione successiva.<br/>                                                                     |
| Estensioni        | Per specificare le proprietà personalizzate desiderate. Il certificato può includere un numero qualsiasi di campi di estensione. Presente solo nella versione X. 509 3,0.<br/>                                            |



 

> [!Note]  
> Servizi certificati Microsoft rilascia certificati X. 509 versione 3.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà nome](name-properties.md)
</dt> </dl>

 

 
