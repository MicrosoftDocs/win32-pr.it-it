---
description: Illustra i passaggi per decrittografare un messaggio crittografato.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Decrittografia di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600903d7a3060c83cd7cd0a85e92f96efe4fb0cfa30c2936c5546f71138b6854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875691"
---
# <a name="decrypting-data"></a>Decrittografia di dati

Questa sezione illustra i passaggi per decrittografare un messaggio crittografato.

**Per decrittografare un messaggio crittografato**

1.  Ottiene un puntatore al messaggio in busta digitale.
2.  Aprire un archivio certificati.
3.  Dal messaggio recuperare l'identificatore del destinatario (ID).
4.  Usare l'identificatore del destinatario per recuperare il certificato.
5.  Ottenere la chiave privata per il certificato.
6.  Usare la chiave privata per decrittografare la chiave simmetrica (sessione).
7.  Recuperare l'algoritmo di crittografia dal messaggio.
8.  Usando la chiave di sessione decrittografata e l'algoritmo di crittografia, decrittografare i dati.

[**CryptDecryptMessage esegue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) tutte le attività per decrittografare un messaggio. Tuttavia, l'inizializzazione di strutture e altri dati è ancora necessaria.

**Per decrittografare i dati usando CryptDecryptMessage**

1.  Ottenere un puntatore al BLOB crittografato.
2.  Aprire un archivio certificati.
3.  Creare una matrice di archivi certificati.
4.  Inizializzare la [**struttura CRYPT \_ DECRYPT MESSAGE \_ \_ PARA.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)
5.  Chiamare [**CryptDecryptMessage per**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) decrittografare i dati contenuti nel messaggio.

[Programma C di esempio: l'uso di CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa la procedura appena presentata. I commenti mostrano gli elementi di codice che esercitino ogni passaggio della procedura. Per informazioni dettagliate sulla funzione, vedere [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)e per informazioni dettagliate sulla struttura dei dati, vedere [**CRYPT \_ DECRYPT MESSAGE \_ \_ PARA.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)

 

 



