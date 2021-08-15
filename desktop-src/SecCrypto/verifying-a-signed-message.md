---
description: Questi passaggi verificano la firma dei dati firmati.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Verifica di un messaggio firmato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7bfdac1b16351d51197a84c15688b0724340af34681312b9cb9865900b8dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970980"
---
# <a name="verifying-a-signed-message"></a>Verifica di un messaggio firmato

Questi passaggi verificano la firma dei dati firmati. La figura seguente illustra le singole attività che devono essere eseguite, come illustrato nell'elenco che la segue.

![verifica di un messaggio firmato](images/verifmsg.png)

**Per verificare la firma di un messaggio firmato**

1.  Ottiene un puntatore al messaggio firmato.
2.  Aprire un [*archivio certificati*](../secgloss/c-gly.md).
3.  Usando l'ID firmatario contenuto nel messaggio, ottenere il certificato del mittente e ottenere un handle per la [*chiave pubblica*](../secgloss/p-gly.md).

    In alternativa ai passaggi 2 e 3, è possibile usare il certificato contenuto nel messaggio per recuperare la chiave pubblica del firmatario.

4.  Usando la chiave pubblica del firmatario, decrittografare la firma digitale, producendo il digest originale dei dati nel messaggio.
5.  Utilizzando l'algoritmo hash contenuto nel messaggio, [*hash*](../secgloss/h-gly.md) dei dati contenuti nel messaggio, generando un nuovo digest.
6.  Confrontare il digest recuperato dal messaggio con il nuovo digest appena creato.
7.  Se i due digest corrispondono, la firma viene verificata. Ciò significa che la chiave [*privata*](../secgloss/p-gly.md) usata per firmare i dati corrisponde alla chiave pubblica usata per decrittografare la firma e che i dati non sono stati modificati dopo la firma dei dati.

    Se i due digest non corrispondono, la firma non viene verificata e le chiavi private/pubbliche non corrispondono oppure i dati sono stati modificati dopo la firma dei dati o entrambi.

È possibile usare [**una singola funzione, CryptVerifyMessageSignature,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)per verificare una firma, come illustrato nella procedura seguente.

**Per verificare un messaggio firmato**

1.  Ottiene un puntatore al messaggio firmato.
2.  Ottiene le dimensioni del messaggio firmato.
3.  Ottenere un handle per un provider del servizio di crittografia.
4.  Inizializzare la [**struttura CRYPT \_ VERIFY MESSAGE \_ \_ PARA.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para)
5.  Chiamare [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) per verificare la firma.

Il codice che implementa questa procedura è incluso nel programma C di esempio: firma di [un messaggio e verifica della firma di un messaggio.](example-c-program-signing-a-message-and-verifying-a-message-signature.md)

 

 
