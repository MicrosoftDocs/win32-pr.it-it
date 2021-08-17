---
description: Il client deve inviare al server una risposta di richiesta digest quando riceve una richiesta digest in risposta a una richiesta per una risorsa.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Contenuto di una risposta di richiesta digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2a4fd199dfe9e97d69628adb0e6012bc4941929b9c1e96e00de8c42d53eba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141154"
---
# <a name="contents-of-a-digest-challenge-response"></a>Contenuto di una risposta di richiesta digest

Il client deve inviare al server una risposta di richiesta digest quando riceve una richiesta digest in risposta a una richiesta per una risorsa. Il client deve inviare nuovamente la richiesta, fornendo un'intestazione Authorization con la risposta di richiesta. Nella tabella seguente vengono descritte le direttive che costituiscono una risposta di richiesta digest.



| Direttiva          | Descrizione                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | Nome dell'account [*dell'entità di sicurezza*](/windows/desktop/SecGloss/s-gly) che richiede la risorsa.                                                                  |
| Realm              | Nome del dominio che contiene l'account indicato dal nome utente.                                                                                                                                                    |
| nonce              | Nonce ricevuto nella richiesta digest.                                                                                                                                                                                |
| Uri                | URI (Universal Resource Identifier) della risorsa richiesta.                                                                                                                                                         |
| qop                | Qualità [della protezione.](quality-of-protection.md)                                                                                                                                                                    |
| Nc                 | Conteggio nonce. Numero di volte in cui il client ha inviato una risposta di richiesta usando il nonce. Per altre informazioni, vedere la direttiva nonce.                                                                              |
| cnonce             | Valore codificato univoco generato dal client per ogni risposta di richiesta.                                                                                                                                                |
| response           | Valore calcolato in base alla specifica digest access ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Una risposta accurata è la prova definitiva che la password dell'utente è nota sul lato client. |
| algoritmo          | Algoritmo ricevuto nella richiesta digest.                                                                                                                                                                            |
| Opaco             | Valore opaco ricevuto nella richiesta digest.                                                                                                                                                                         |
| Crittografia (solo SASL) | Uno dei valori di crittografia ricevuti nella richiesta digest. Per informazioni dettagliate sulla crittografia, vedere [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).                                                             |



 

Microsoft Digest supporta i moduli nome utente/area di autenticazione seguenti:

-   Area di autenticazione del nome utente
-   Dominio AccountName (flat)
-   UPN "" (vuoto)
-   NetBIOS "" (vuoto)

Sebbene siano supportati caratteri maiuscoli, per ottenere prestazioni ottimali corrispondenti ai valori hash digest precalcolati del server, è consigliabile usare caratteri minuscoli.

L'uso di hash precalcolati è una nuova funzionalità che consente agli operatori di sistema di ignorare l'uso di password crittografate reversibili nel controller di dominio. Un hash precalcoato viene formato per un utente quando viene modificata la password dell'utente.

Microsoft Digest genera la stringa di risposta di richiesta digest per le applicazioni client. Per informazioni dettagliate, vedere [Generazione della risposta di richiesta digest](generating-the-digest-challenge-response.md).

 

 
