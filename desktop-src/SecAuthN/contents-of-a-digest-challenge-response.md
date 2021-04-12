---
description: Il client deve inviare al server una risposta di verifica del digest quando riceve una richiesta di verifica del digest in risposta a una richiesta di una risorsa.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Contenuto di una risposta di richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232043"
---
# <a name="contents-of-a-digest-challenge-response"></a>Contenuto di una risposta di richiesta digest

Il client deve inviare al server una risposta di verifica del digest quando riceve una richiesta di verifica del digest in risposta a una richiesta di una risorsa. Il client deve inviare nuovamente la richiesta, fornendo un'intestazione di autorizzazione con la risposta alla richiesta di verifica. Nella tabella seguente vengono descritte le direttive che costituiscono una risposta di verifica del digest.



| Direttiva          | Descrizione                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | Nome dell'account dell' [*entità di sicurezza*](/windows/desktop/SecGloss/s-gly) che richiede la risorsa.                                                                  |
| Realm              | Nome del dominio che contiene l'account indicato dal nome utente.                                                                                                                                                    |
| nonce              | Nonce ricevuto nella richiesta digest.                                                                                                                                                                                |
| Uri                | URI (Universal Resource Identifier) della risorsa richiesta.                                                                                                                                                         |
| qop                | [Qualità della protezione](quality-of-protection.md).                                                                                                                                                                    |
| NC                 | Conteggio dei nonce. Numero di volte in cui il client ha inviato una risposta di verifica tramite il parametro nonce. Per ulteriori informazioni, vedere la direttiva nonce.                                                                              |
| cnonce             | Valore codificato univoco generato dal client per ogni risposta alla richiesta di verifica.                                                                                                                                                |
| response           | Valore calcolato in base alla specifica di accesso digest ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Una risposta accurata è una prova definitiva che indica che la password dell'utente è nota sul lato client. |
| algoritmo          | Algoritmo ricevuto nella richiesta digest.                                                                                                                                                                            |
| opaco             | Valore opaco ricevuto nella richiesta digest.                                                                                                                                                                         |
| Crittografia (solo SASL) | Uno dei valori di crittografia ricevuti nella richiesta digest. Per informazioni dettagliate sulla crittografia, vedere [qualità della protezione e crittografie](quality-of-protection-and-ciphers.md).                                                             |



 

Microsoft Digest supporta i seguenti formati di nome utente/area di autenticazione:

-   Area di autenticazione nome utente
-   Dominio AccountName (Flat)
-   UPN "" (vuoto)
-   NetBIOS "" (vuoto)

Mentre i caratteri maiuscoli sono supportati, per ottenere prestazioni ottimali corrispondenti ai valori hash digest precalcolati del server, è consigliabile usare caratteri minuscoli.

L'utilizzo di hash precalcolati è una nuova funzionalità che consente agli operatori di sistema di ignorare l'utilizzo di password crittografate reversibili sul controller di dominio. Un hash precalcolato viene formato per un utente quando la password dell'utente viene modificata.

Microsoft Digest genera la stringa di risposta di richiesta digest per le applicazioni client. Per informazioni dettagliate, vedere [generazione della risposta di verifica del digest](generating-the-digest-challenge-response.md).

 

 
