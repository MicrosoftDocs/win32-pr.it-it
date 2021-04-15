---
description: Vengono illustrati i passaggi per decrittografare un messaggio crittografato.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Decrittografia di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350156"
---
# <a name="decrypting-data"></a>Decrittografia di dati

In questa sezione vengono illustrati i passaggi per decrittografare un messaggio crittografato.

**Per decrittografare un messaggio crittografato**

1.  Ottenere un puntatore al messaggio in busta digitale.
2.  Aprire un archivio certificati.
3.  Dal messaggio recuperare l'identificatore del destinatario (ID).
4.  Utilizzare l'identificatore del destinatario per recuperare il certificato.
5.  Ottenere la chiave privata per il certificato.
6.  Utilizzare la chiave privata per decrittografare la chiave simmetrica (sessione).
7.  Recuperare l'algoritmo di crittografia dal messaggio.
8.  Utilizzando la chiave della sessione decrittografata e l'algoritmo di crittografia, decrittografare i dati.

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) esegue tutte le attività per la decrittografia di un messaggio. Tuttavia, l'inizializzazione di strutture e altri dati è ancora necessaria.

**Per decrittografare i dati tramite CryptDecryptMessage**

1.  Ottenere un puntatore al BLOB crittografato.
2.  Aprire un archivio certificati.
3.  Creare una matrice dell'archivio certificati.
4.  Inizializzare la struttura [**\_ paracrypt \_ message \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) paracrypt.
5.  Chiamare [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per decrittografare i dati contenuti nel messaggio.

[Esempio di programma C: l'utilizzo di CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa la procedura appena presentata. I commenti mostrano gli elementi di codice che eseguono ogni passaggio della procedura. Per informazioni dettagliate sulla funzione, vedere [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)e per informazioni dettagliate sulla struttura dei dati, vedere [**crypt \_ Decrypt \_ message \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 



