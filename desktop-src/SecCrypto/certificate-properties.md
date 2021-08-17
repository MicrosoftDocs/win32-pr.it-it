---
description: Servizi certificati supporta l'uso di certificati come definito nella raccomandazione ITU-T X.509 (anche ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Proprietà certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48850b812c8a8227f41229ccbaa88259805d61a199d695f4a90d4652a94b99dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771566"
---
# <a name="certificate-properties"></a>Proprietà certificato

Servizi certificati supporta l'uso di certificati come definito nella raccomandazione ITU-T [*X.509*](../secgloss/x-gly.md) (anche ISO/IEC 9594-8). Di seguito sono riportate le proprietà contenute in un certificato X.509 standard.



| Campo                                       | Descrizione                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione                                     | Numero di versione del formato del certificato.                                                                                                                                                                       |
| Numero di serie                               | Numero di serie del certificato. Questo numero viene assegnato dall'autorità emittente ed è univoco all'interno dell'elenco dei certificati emessi dell'emittente.                                                                          |
| Identificatore e parametri dell'algoritmo         | Algoritmo di firma ed eventuali parametri usati dall'autorità emittente.                                                                                                                                                      |
| Issuer                                      | Nome [*dell'autorità di certificazione che*](../secgloss/c-gly.md) ha emesso il certificato.                                               |
| Non prima (data)                           | Certificato non valido prima di questa data.                                                                                                                                                                         |
| Non dopo (data)                            | Certificato non valido dopo questa data.                                                                                                                                                                          |
| Nome soggetto                                | Nome della persona o dell'entità a cui viene emesso il certificato. Questo campo può includere anche l'organizzazione, l'unità organizzativa, la zona, lo stato o la provincia del destinatario del certificato e il paese/area geografica. |
| Algoritmo e parametri della chiave pubblica del soggetto | Algoritmo ed eventuali parametri utilizzati per la chiave pubblica [*del soggetto.*](../secgloss/p-gly.md)                                                                       |
| Chiave pubblica dell'oggetto                          | Chiave pubblica effettiva (una stringa di bit).                                                                                                                                                                           |
| Firma                                   | Firma fornita dall'autorità emittente.                                                                                                                                                                            |



 

Un certificato può contenere gli elementi seguenti, a seconda della [*versione X.509*](../secgloss/x-gly.md) del certificato.



| Campo facoltativo    | Descrizione                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID univoco dell'autorità di emittente  | Usato per rendere il nome dell'autorità emittente non ambiguo se è stato usato da più di un'entità. Presente solo nelle [*versioni X.509*](../secgloss/x-gly.md) 2.0 o successive.<br/> |
| ID univoco del soggetto | Usato per rendere il nome soggetto non ambiguo se è stato usato da più di un'entità. Presente solo in X.509 2.0 o versione successiva.<br/>                                                                     |
| Estensioni        | Per specificare le proprietà personalizzate desiderate. Nel certificato può essere incluso un numero qualsiasi di campi di estensione. Presente solo nella versione X.509 3.0.<br/>                                            |



 

> [!Note]  
> Servizi certificati Microsoft emessi certificati X.509 versione 3.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà nome](name-properties.md)
</dt> </dl>

 

 
