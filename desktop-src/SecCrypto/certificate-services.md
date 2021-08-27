---
description: Servizi certificati, un servizio in esecuzione in un sistema operativo server Windows, riceve le richieste di nuovi certificati digitali su trasporti come RPC o HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaac2e1ee01b588beedbe2e632e52ef41459a885782a7975e460182f8a211bef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126851"
---
# <a name="certificate-services"></a>Servizi certificati

[*Servizi certificati,*](../secgloss/c-gly.md)un servizio in esecuzione in un sistema operativo server Windows, riceve le richieste di nuovi certificati digitali su trasporti come RPC o HTTP. Controlla ogni richiesta rispetto a criteri personalizzati o specifici del sito, imposta le proprietà facoltative per l'emissione di un certificato ed elava il certificato. Servizi certificati consente agli amministratori di aggiungere elementi a un elenco di [*revoche*](../secgloss/c-gly.md) di certificati (CRL) e di pubblicare regolarmente elenchi di revoche di certificati firmati.

I servizi certificati includono interfacce programmabili per la creazione del supporto per trasporti aggiuntivi, criteri e proprietà e formati dei certificati.

In Windows Server 2003 è possibile installare Servizi certificati 2.0 da  **Pannello di controllo** facendo clic su Installazione applicazioni e quindi su Installazione componenti **di Windows** per installare o disinstallare Servizi certificati.

I concetti relativi a Servizi certificati sono descritti in dettaglio nelle sezioni seguenti. Il contenuto è utile per sviluppare applicazioni che interagiranno con Servizi certificati.



| Content                                                                                                                                                           | Sezione                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Descrizione delle funzionalità di Servizi certificati                                                                                                               | [Funzionalità di Servizi certificati](certificate-services-features.md)         |
| Panoramica dell'architettura di Servizi certificati                                                                                                                     | [Architettura di Servizi certificati](certificate-services-architecture.md) |
| Relazione tra un certificato, il soggetto del certificato e la chiave pubblica [ *del soggetto*](../secgloss/p-gly.md) | [Certificati e chiavi pubbliche](certificates-and-public-keys.md)           |
| Informazioni sulle proprietà della richiesta di certificato                                                                                                              | [Linee guida per le richieste di certificati](certificate-request-guidelines.md)       |
| Informazioni dettagliate sull'elaborazione di un certificato da parte di Servizi certificati                                                                                                 | [Informazioni sui certificati](about-certificates.md)                               |
| Descrizione del processo [*di rinnovo dell'autorità*](../secgloss/c-gly.md) di certificazione        | [Rinnovo dell'autorità di certificazione](certification-authority-renewal.md)     |



 

Sono inclusi anche gli argomenti aggiuntivi seguenti.



| Content                                                                                                                                             | Sezione                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Documentazione sul controllo di registrazione certificati, che fornisce servizi per la creazione di richieste di certificati, incluse le richieste smart card utenti. | [Controllo registrazione certificati](certificate-enrollment-control.md) |
| Documentazione su Microsoft Cryptographic Application Programming Interface, che fornisce servizi di sicurezza basati sulla crittografia.                | [Informazioni di base sulla crittografia](cryptography-essentials.md)               |
| Documentazione sulla smart card, che fornisce servizi per lo sviluppo e l'smart card sistemi.                                                   | [Smart card](../secauthn/smart-card-authentication.md)                     |
| Proprietà dei nomi dei certificati e delle richieste di certificati.                                                                                           | [Proprietà nome](name-properties.md)                               |
| Elenco e descrizioni delle [*proprietà del certificato X.509.*](../secgloss/x-gly.md)                                  | [Proprietà del certificato](certificate-properties.md)                 |



 

 

 
