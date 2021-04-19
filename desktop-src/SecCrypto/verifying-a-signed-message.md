---
description: Questi passaggi verificano la firma dei dati firmati.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Verifica di un messaggio firmato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317691"
---
# <a name="verifying-a-signed-message"></a>Verifica di un messaggio firmato

Questi passaggi verificano la firma dei dati firmati. Nella figura seguente vengono illustrate le singole attività che devono essere eseguite, come illustrato nell'elenco che segue.

![Verifica di un messaggio firmato](images/verifmsg.png)

**Per verificare la firma di un messaggio firmato**

1.  Ottenere un puntatore al messaggio firmato.
2.  Aprire un [*archivio certificati*](../secgloss/c-gly.md).
3.  Utilizzando l'ID del firmatario contenuto nel messaggio, ottenere il certificato del mittente e ottenere un handle per la relativa [*chiave pubblica*](../secgloss/p-gly.md).

    In alternativa ai passaggi 2 e 3, è possibile usare il certificato contenuto nel messaggio per recuperare la chiave pubblica del firmatario.

4.  Utilizzando la chiave pubblica del firmatario, decrittografare la firma digitale, producendo il digest originale dei dati nel messaggio.
5.  Utilizzando l'algoritmo hash contenuto nel messaggio, viene eseguito l' [*hashing*](../secgloss/h-gly.md) dei dati contenuti nel messaggio, restituendo un nuovo digest.
6.  Confrontare il digest recuperato dal messaggio con il nuovo digest appena creato.
7.  Se i due digest corrispondono, la firma viene verificata. Ciò significa che la [*chiave privata*](../secgloss/p-gly.md) usata per firmare i dati corrisponde alla chiave pubblica appena usata per decrittografare la firma e che i dati non sono stati modificati dopo la firma dei dati.

    Se i due digest non corrispondono, la firma non viene verificata e le chiavi private/pubbliche non corrispondono oppure i dati sono stati modificati dopo la firma dei dati o entrambi.

Una singola funzione, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), può essere usata per verificare una firma, come illustrato nella procedura seguente.

**Per verificare un messaggio firmato**

1.  Ottenere un puntatore al messaggio firmato.
2.  Ottiene le dimensioni del messaggio firmato.
3.  Ottenere un handle per un provider di crittografia.
4.  Inizializzare la struttura della [**\_ \_ \_ paragrafi di verifica del messaggio di crittografia**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) .
5.  Chiamare [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) per verificare la firma.

Il codice che implementa questa procedura è incluso nel [programma C di esempio: firma di un messaggio e verifica della firma di un messaggio](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
