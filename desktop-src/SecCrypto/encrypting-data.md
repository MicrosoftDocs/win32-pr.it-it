---
description: Descrive i passaggi da eseguire per crittografare un messaggio con le funzioni di crittografia di base.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Crittografia dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d2a7fde500397959f0a2352b3f8ddb4fa662209afb251ddceaa8774048f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874456"
---
# <a name="encrypting-data"></a>Crittografia dei dati

La procedura seguente descrive i passaggi da eseguire per crittografare un messaggio con le funzioni di crittografia di base. Per crittografare i messaggi usando gli standard PKCS 7, vedere Funzioni dei messaggi di basso livello \# e [Funzioni messaggi semplificate](cryptography-functions.md). [](cryptography-functions.md)

**Per crittografare un messaggio**

1.  Generare una chiave di sessione usando la [**funzione CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)

    Questa chiamata genera una chiave casuale e restituisce un handle in modo che la chiave possa essere usata per crittografare e decrittografare i dati. A questo punto viene specificato anche l'algoritmo di crittografia da usare. Poiché CryptoAPI non consente alle applicazioni di usare algoritmi a chiave pubblica per crittografare i dati bulk, specificare un algoritmo simmetrico, ad esempio RC2 o RC4 con la chiamata [**CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)

2.  In alternativa, usare la [**funzione CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) per trasformare una password in una chiave adatta per la crittografia.

    Se un'applicazione deve crittografare il messaggio in modo che chiunque abbia una password specificata possa decrittografare i dati, usare [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) per trasformare la password in una chiave adatta per la crittografia.

    > [!Note]  
    > In questo caso, questa funzione viene chiamata al posto della funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) e le chiamate [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) successive non sono necessarie.

     

3.  Se necessario, impostare proprietà di crittografia aggiuntive della chiave usando la [**funzione CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)

    Dopo la generazione della chiave, è possibile impostare proprietà crittografiche aggiuntive della chiave con la [**funzione CryptSetKeyParam.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) Questa funzione consente di crittografare diverse sezioni del file con salti di chiave diversi e consente di modificare la modalità di crittografia o il vettore di inizializzazione della chiave. Questi parametri possono essere usati per rendere la crittografia conforme a uno standard di crittografia dei dati specifico.

4.  Crittografare i dati nel file con [**la funzione CryptEncrypt.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt)

    La [**funzione CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) accetta la chiave di sessione generata nel passaggio precedente e crittografa un buffer di dati.

    > [!Note]  
    > Quando i dati vengono crittografati, i dati possono essere leggermente espansi dall'algoritmo di crittografia. L'applicazione è responsabile della memoria della lunghezza dei dati crittografati in modo che la lunghezza corretta possa essere specificata in un secondo momento per la [**funzione CryptDecrypt.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt)

     

5.  Facoltativamente, usare la [**funzione CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) per consentire all'utente corrente di decrittografare i dati in futuro.

    Per consentire all'utente corrente di decrittografare i dati in futuro, la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) viene usata per salvare la chiave di decrittografia in un formato crittografato (BLOB di chiavi) che può essere decrittografato solo con la chiave privata dell'utente. Questa funzione richiede la chiave pubblica dello scambio di chiavi dell'utente a questo scopo, che può essere ottenuta usando la [**funzione CryptGetUserKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) La **funzione CryptExportKey** restituirà un BLOB di chiavi che deve essere archiviato dall'applicazione per l'uso nella decrittografia del file

> [!Note]  
> Se l'applicazione ha certificati (o chiavi pubbliche) per altri utenti, può consentire ad altri utenti di decrittografare il file eseguendo chiamate [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) per ogni utente che deve ricevere l'accesso. I BLOB delle chiavi restituiti devono essere archiviati dall'applicazione, come nel passaggio 5.

 

## <a name="creating-an-encrypted-message"></a>Creazione di un messaggio crittografato

Le funzioni di messaggio semplificate semplificano la crittografia e la decrittografia dei dati. La figura seguente illustra le singole attività che devono essere eseguite per crittografare un messaggio. I passaggi sono descritti nell'elenco seguente.

![crittografia di un messaggio](images/encmsg.png)

**Per crittografare un messaggio**

1.  Ottenere un puntatore al messaggio di testo non crittografato.
2.  Generare una chiave simmetrica (sessione).
3.  Usando la chiave simmetrica e l'algoritmo di crittografia specificato, crittografare i dati del messaggio.
4.  Aprire un archivio certificati.
5.  Ottenere il certificato del destinatario.
6.  Ottenere la chiave pubblica dal certificato del destinatario.
7.  Usando la chiave pubblica del destinatario, crittografare la chiave simmetrica.
8.  Ottenere l'identificatore del destinatario dal certificato del destinatario.
9.  Includere quanto segue nel messaggio con busta digitale: l'algoritmo di crittografia dei dati, i dati crittografati, la chiave simmetrica crittografata e l'identificatore del destinatario.

 

 



