---
description: Servizi certificati, un servizio in esecuzione in un sistema operativo Windows Server, riceve le richieste di nuovi certificati digitali su trasporti quali RPC o HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315813"
---
# <a name="certificate-services"></a>Servizi certificati

[*Servizi certificati*](../secgloss/c-gly.md), un servizio in esecuzione in un sistema operativo Windows Server, riceve le richieste di nuovi certificati digitali su trasporti quali RPC o http. Verifica ogni richiesta rispetto a criteri personalizzati o specifici del sito, imposta le proprietà facoltative per un certificato da emettere e rilascia il certificato. Servizi certificati consente agli amministratori di aggiungere elementi a un [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL) e di pubblicare i CRL firmati a intervalli regolari.

I servizi certificati includono interfacce programmabili per la creazione del supporto per trasporti, criteri e proprietà e formati di certificati aggiuntivi.

In Windows Server 2003, è possibile installare Servizi certificati 2,0 dal **Pannello di controllo** facendo clic su **Installazione applicazioni** e quindi su **Aggiungi/Rimuovi componenti di Windows** per installare o disinstallare Servizi certificati.

I concetti relativi ai Servizi certificati sono descritti in dettaglio nelle sezioni seguenti. Il contenuto è concepito per semplificare lo sviluppo di applicazioni che interagiranno con servizi certificati.



| Content                                                                                                                                                           | Sezione                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Descrizione delle funzionalità di Servizi certificati                                                                                                               | [Funzionalità di Servizi certificati](certificate-services-features.md)         |
| Panoramica dell'architettura di Servizi certificati                                                                                                                     | [Architettura di Servizi certificati](certificate-services-architecture.md) |
| Relazione tra un certificato, l'oggetto del certificato e la [ *chiave pubblica* del soggetto](../secgloss/p-gly.md) | [Certificati e chiavi pubbliche](certificates-and-public-keys.md)           |
| Informazioni sulle proprietà della richiesta di certificato                                                                                                              | [Linee guida per le richieste di certificati](certificate-request-guidelines.md)       |
| Dettagli della modalità di elaborazione di un certificato da Servizi certificati                                                                                                 | [Informazioni sui certificati](about-certificates.md)                               |
| Descrizione del processo di rinnovo dell' [*autorità di certificazione*](../secgloss/c-gly.md)        | [Rinnovo dell'autorità di certificazione](certification-authority-renewal.md)     |



 

Sono inclusi anche i seguenti argomenti utili aggiuntivi.



| Content                                                                                                                                             | Sezione                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Documentazione relativa al controllo di registrazione certificati, che fornisce servizi per la creazione di richieste di certificati, incluse le richieste per gli utenti di smart card. | [Controllo di registrazione certificati](certificate-enrollment-control.md) |
| Documentazione sull'interfaccia di programmazione dell'applicazione di crittografia Microsoft, che fornisce servizi di sicurezza basati su crittografia.                | [Crittografia Essentials](cryptography-essentials.md)               |
| Documentazione su smart card, che fornisce servizi per lo sviluppo e l'utilizzo di sistemi di smart card.                                                   | [Smart card](../secauthn/smart-card-authentication.md)                     |
| Nome delle proprietà dei certificati e delle richieste di certificati.                                                                                           | [Proprietà nome](name-properties.md)                               |
| Elenco e descrizioni delle proprietà del certificato [*X. 509*](../secgloss/x-gly.md) .                                  | [Proprietà certificato](certificate-properties.md)                 |



 

 

 
