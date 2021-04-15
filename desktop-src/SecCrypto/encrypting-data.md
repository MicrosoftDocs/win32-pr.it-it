---
description: Descrive i passaggi da eseguire per crittografare un messaggio con le funzioni di crittografia di base.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Crittografia dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561704"
---
# <a name="encrypting-data"></a>Crittografia dei dati

Nella procedura riportata di seguito vengono descritti i passaggi da eseguire per crittografare un messaggio con le funzioni di crittografia di base. Per crittografare i messaggi usando \# gli standard PKCS 7, vedere [funzioni di messaggio di basso livello](cryptography-functions.md) e funzioni di [messaggio semplificate](cryptography-functions.md).

**Per crittografare un messaggio**

1.  Generare una chiave di sessione tramite la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .

    Questa chiamata genera una chiave casuale e restituisce un handle in modo che la chiave possa essere usata per crittografare e decrittografare i dati. A questo punto viene specificato anche l'algoritmo di crittografia da usare. Poiché CryptoAPI non consente alle applicazioni di usare algoritmi a chiave pubblica per crittografare i dati in blocco, specificare un algoritmo simmetrico come RC2 o RC4 con la chiamata [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .

2.  In alternativa, usare la funzione [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) per trasformare una password in una chiave adatta per la crittografia.

    Se un'applicazione deve crittografare il messaggio in modo che chiunque disponga di una password specificata possa decrittografare i dati, usare [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) per trasformare la password in una chiave adatta per la crittografia.

    > [!Note]  
    > In questo caso, questa funzione viene chiamata al posto della funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) e le chiamate [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) successive non sono necessarie.

     

3.  Se necessario, impostare le proprietà di crittografia aggiuntive della chiave tramite la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)

    Dopo la generazione della chiave, è possibile impostare le proprietà di crittografia aggiuntive della chiave con la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Questa funzione consente a diverse sezioni del file di essere crittografate con Salt di chiave diversi e fornisce un modo per modificare la modalità di crittografia o il vettore di inizializzazione della chiave. Questi parametri possono essere usati per rendere la crittografia conforme a uno standard di crittografia dei dati specifico.

4.  Crittografare i dati nel file con la funzione [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .

    La funzione [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) accetta la chiave di sessione generata nel passaggio precedente e crittografa un buffer di dati.

    > [!Note]  
    > Poiché i dati sono crittografati, i dati possono essere leggermente espansi dall'algoritmo di crittografia. L'applicazione è responsabile di ricordare la lunghezza dei dati crittografati in modo da poter specificare la lunghezza appropriata per la funzione [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .

     

5.  Facoltativamente, utilizzare la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) per consentire all'utente corrente di decrittografare i dati in futuro.

    Per consentire all'utente corrente di decrittografare i dati in futuro, la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) viene usata per salvare la chiave di decrittografia in un formato crittografato (un BLOB di chiavi) che può essere decrittografato solo con la chiave privata dell'utente. Questa funzione richiede la chiave pubblica scambio di chiave dell'utente per questo scopo, che può essere ottenuta tramite la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) . La funzione **CryptExportKey** restituirà un BLOB della chiave che deve essere archiviato dall'applicazione per l'uso nella decrittografia del file

> [!Note]  
> Se l'applicazione dispone di certificati (o chiavi pubbliche) per altri utenti, può consentire ad altri utenti di decrittografare il file eseguendo chiamate [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) per ogni utente che deve ricevere l'accesso. I BLOB di chiavi restituiti devono essere archiviati dall'applicazione, come nel passaggio 5.

 

## <a name="creating-an-encrypted-message"></a>Creazione di un messaggio crittografato

Le funzioni di messaggio semplificate rendono più semplice crittografare e decrittografare i dati. Nella figura seguente vengono illustrate le singole attività che devono essere eseguite per crittografare un messaggio. I passaggi sono descritti nell'elenco seguente.

![crittografia di un messaggio](images/encmsg.png)

**Per crittografare un messaggio**

1.  Ottenere un puntatore al messaggio in testo non crittografato.
2.  Genera una chiave simmetrica (sessione).
3.  Utilizzando la chiave simmetrica e l'algoritmo di crittografia specificato, crittografare i dati del messaggio.
4.  Aprire un archivio certificati.
5.  Ottenere il certificato del destinatario.
6.  Ottenere la chiave pubblica dal certificato del destinatario.
7.  Utilizzando la chiave pubblica del destinatario, crittografare la chiave simmetrica.
8.  Ottenere l'identificatore del destinatario dal certificato del destinatario.
9.  Includere il codice seguente nel messaggio in busta digitale: l'algoritmo di crittografia dei dati, i dati crittografati, la chiave simmetrica crittografata e l'identificatore del destinatario.

 

 



