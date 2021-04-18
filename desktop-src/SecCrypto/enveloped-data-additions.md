---
description: Elenca le modifiche apportate alle funzionalità per l'inviluppo dei dati.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Aggiunte di dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310754"
---
# <a name="enveloped-data-additions"></a>Aggiunte di dati in busta

Sono state apportate le modifiche seguenti alle funzionalità dei dati in busta:

-   L'identificazione del destinatario può essere eseguita non solo dall'emittente e dal numero di serie (PKCS \# 7 1,5), ma anche dall'identificatore di chiave.
-   Sono disponibili tre opzioni di scambio delle chiavi del destinatario:
    -   Trasporto chiavi con chiavi RSA.
    -   Accordo chiave che usa Ephemeral-Static Diffie-Hellman le chiavi dell'algoritmo incapsulate con 3DES o RC2 oppure Ephemeral-Static la curva ellittica Diffie-Hellman chiavi di algoritmo incapsulate con AES.
    -   Trasferimento della chiave di crittografia della chiave o dell'elenco di messaggi in cui la chiave usata per crittografare la chiave di crittografia del contenuto è già stata distribuita ai destinatari. RC2, 3DES e AES sono consentiti come algoritmi di wrapping delle chiavi.
-   Gli attributi non protetti possono essere inclusi nel messaggio.
-   È stato aggiunto un campo **OriginatorInfo** che contiene informazioni sul creatore che può contenere certificati e CRL.
-   Algoritmi basati sulla crittografia a curva ellittica (ECC) e AES richiedono Windows Vista o versioni successive.

 

 



