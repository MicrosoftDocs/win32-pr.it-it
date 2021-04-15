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
# <a name="encrypting-data"></a><span data-ttu-id="751a9-103">Crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="751a9-103">Encrypting Data</span></span>

<span data-ttu-id="751a9-104">Nella procedura riportata di seguito vengono descritti i passaggi da eseguire per crittografare un messaggio con le funzioni di crittografia di base.</span><span class="sxs-lookup"><span data-stu-id="751a9-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="751a9-105">Per crittografare i messaggi usando \# gli standard PKCS 7, vedere [funzioni di messaggio di basso livello](cryptography-functions.md) e funzioni di [messaggio semplificate](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="751a9-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="751a9-106">**Per crittografare un messaggio**</span><span class="sxs-lookup"><span data-stu-id="751a9-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="751a9-107">Generare una chiave di sessione tramite la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="751a9-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="751a9-108">Questa chiamata genera una chiave casuale e restituisce un handle in modo che la chiave possa essere usata per crittografare e decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="751a9-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="751a9-109">A questo punto viene specificato anche l'algoritmo di crittografia da usare.</span><span class="sxs-lookup"><span data-stu-id="751a9-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="751a9-110">Poiché CryptoAPI non consente alle applicazioni di usare algoritmi a chiave pubblica per crittografare i dati in blocco, specificare un algoritmo simmetrico come RC2 o RC4 con la chiamata [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="751a9-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="751a9-111">In alternativa, usare la funzione [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) per trasformare una password in una chiave adatta per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="751a9-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="751a9-112">Se un'applicazione deve crittografare il messaggio in modo che chiunque disponga di una password specificata possa decrittografare i dati, usare [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) per trasformare la password in una chiave adatta per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="751a9-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="751a9-113">In questo caso, questa funzione viene chiamata al posto della funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) e le chiamate [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) successive non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="751a9-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="751a9-114">Se necessario, impostare le proprietà di crittografia aggiuntive della chiave tramite la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)</span><span class="sxs-lookup"><span data-stu-id="751a9-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="751a9-115">Dopo la generazione della chiave, è possibile impostare le proprietà di crittografia aggiuntive della chiave con la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="751a9-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="751a9-116">Questa funzione consente a diverse sezioni del file di essere crittografate con Salt di chiave diversi e fornisce un modo per modificare la modalità di crittografia o il vettore di inizializzazione della chiave.</span><span class="sxs-lookup"><span data-stu-id="751a9-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="751a9-117">Questi parametri possono essere usati per rendere la crittografia conforme a uno standard di crittografia dei dati specifico.</span><span class="sxs-lookup"><span data-stu-id="751a9-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="751a9-118">Crittografare i dati nel file con la funzione [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="751a9-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="751a9-119">La funzione [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) accetta la chiave di sessione generata nel passaggio precedente e crittografa un buffer di dati.</span><span class="sxs-lookup"><span data-stu-id="751a9-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="751a9-120">Poiché i dati sono crittografati, i dati possono essere leggermente espansi dall'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="751a9-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="751a9-121">L'applicazione è responsabile di ricordare la lunghezza dei dati crittografati in modo da poter specificare la lunghezza appropriata per la funzione [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="751a9-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="751a9-122">Facoltativamente, utilizzare la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) per consentire all'utente corrente di decrittografare i dati in futuro.</span><span class="sxs-lookup"><span data-stu-id="751a9-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="751a9-123">Per consentire all'utente corrente di decrittografare i dati in futuro, la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) viene usata per salvare la chiave di decrittografia in un formato crittografato (un BLOB di chiavi) che può essere decrittografato solo con la chiave privata dell'utente.</span><span class="sxs-lookup"><span data-stu-id="751a9-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="751a9-124">Questa funzione richiede la chiave pubblica scambio di chiave dell'utente per questo scopo, che può essere ottenuta tramite la funzione [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) .</span><span class="sxs-lookup"><span data-stu-id="751a9-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="751a9-125">La funzione **CryptExportKey** restituirà un BLOB della chiave che deve essere archiviato dall'applicazione per l'uso nella decrittografia del file</span><span class="sxs-lookup"><span data-stu-id="751a9-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="751a9-126">Se l'applicazione dispone di certificati (o chiavi pubbliche) per altri utenti, può consentire ad altri utenti di decrittografare il file eseguendo chiamate [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) per ogni utente che deve ricevere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="751a9-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="751a9-127">I BLOB di chiavi restituiti devono essere archiviati dall'applicazione, come nel passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="751a9-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="751a9-128">Creazione di un messaggio crittografato</span><span class="sxs-lookup"><span data-stu-id="751a9-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="751a9-129">Le funzioni di messaggio semplificate rendono più semplice crittografare e decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="751a9-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="751a9-130">Nella figura seguente vengono illustrate le singole attività che devono essere eseguite per crittografare un messaggio.</span><span class="sxs-lookup"><span data-stu-id="751a9-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="751a9-131">I passaggi sono descritti nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="751a9-131">The steps are described in the following list.</span></span>

![crittografia di un messaggio](images/encmsg.png)

<span data-ttu-id="751a9-133">**Per crittografare un messaggio**</span><span class="sxs-lookup"><span data-stu-id="751a9-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="751a9-134">Ottenere un puntatore al messaggio in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="751a9-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="751a9-135">Genera una chiave simmetrica (sessione).</span><span class="sxs-lookup"><span data-stu-id="751a9-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="751a9-136">Utilizzando la chiave simmetrica e l'algoritmo di crittografia specificato, crittografare i dati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="751a9-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="751a9-137">Aprire un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="751a9-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="751a9-138">Ottenere il certificato del destinatario.</span><span class="sxs-lookup"><span data-stu-id="751a9-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="751a9-139">Ottenere la chiave pubblica dal certificato del destinatario.</span><span class="sxs-lookup"><span data-stu-id="751a9-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="751a9-140">Utilizzando la chiave pubblica del destinatario, crittografare la chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="751a9-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="751a9-141">Ottenere l'identificatore del destinatario dal certificato del destinatario.</span><span class="sxs-lookup"><span data-stu-id="751a9-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="751a9-142">Includere il codice seguente nel messaggio in busta digitale: l'algoritmo di crittografia dei dati, i dati crittografati, la chiave simmetrica crittografata e l'identificatore del destinatario.</span><span class="sxs-lookup"><span data-stu-id="751a9-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



