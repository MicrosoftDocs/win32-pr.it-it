---
description: Elenca le modifiche apportate alle funzionalità per l'avvolso dei dati.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Aggiunte di dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75aab8e931ff8c8591a899a21a1071754e32f2e2cecec3755baa3dc64db94dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874421"
---
# <a name="enveloped-data-additions"></a>Aggiunte di dati in busta

Alle funzionalità dei dati in busta sono state apportate le modifiche seguenti:

-   L'identificazione del destinatario può essere eseguita non solo dall'autorità emittente e dal numero di serie (PKCS \# 7 1.5), ma anche dall'identificatore di chiave.
-   Sono disponibili tre opzioni di scambio delle chiavi del destinatario:
    -   Trasporto delle chiavi con chiavi RSA.
    -   Contratto di chiave usando chiavi Ephemeral-Static Diffie-Hellman algoritmo incapsulate con 3DES o RC2 o chiavi dell'algoritmo Ephemeral-Static curva ellittica Diffie-Hellman incapsulate con AES.
    -   Key Encryption Key o Mail List key transfer in cui la chiave usata per crittografare la chiave di crittografia del contenuto è già stata distribuita ai destinatari. RC2, 3DES e AES sono consentiti come algoritmi di wrapping delle chiavi.
-   Gli attributi non protetti possono essere inclusi nel messaggio.
-   È stato aggiunto un campo **OriginatorInfo** contenente informazioni sull'iniziatore che possono contenere certificati e CRL.
-   Gli algoritmi basati su ECC (Elliptic Curve Cryptography) e AES Windows Vista o versioni successive.

 

 



