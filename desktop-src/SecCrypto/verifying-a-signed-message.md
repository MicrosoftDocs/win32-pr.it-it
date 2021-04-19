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
# <a name="verifying-a-signed-message"></a><span data-ttu-id="6a8fb-103">Verifica di un messaggio firmato</span><span class="sxs-lookup"><span data-stu-id="6a8fb-103">Verifying a Signed Message</span></span>

<span data-ttu-id="6a8fb-104">Questi passaggi verificano la firma dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="6a8fb-105">Nella figura seguente vengono illustrate le singole attività che devono essere eseguite, come illustrato nell'elenco che segue.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![Verifica di un messaggio firmato](images/verifmsg.png)

<span data-ttu-id="6a8fb-107">**Per verificare la firma di un messaggio firmato**</span><span class="sxs-lookup"><span data-stu-id="6a8fb-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="6a8fb-108">Ottenere un puntatore al messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="6a8fb-109">Aprire un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6a8fb-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="6a8fb-110">Utilizzando l'ID del firmatario contenuto nel messaggio, ottenere il certificato del mittente e ottenere un handle per la relativa [*chiave pubblica*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6a8fb-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="6a8fb-111">In alternativa ai passaggi 2 e 3, è possibile usare il certificato contenuto nel messaggio per recuperare la chiave pubblica del firmatario.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="6a8fb-112">Utilizzando la chiave pubblica del firmatario, decrittografare la firma digitale, producendo il digest originale dei dati nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="6a8fb-113">Utilizzando l'algoritmo hash contenuto nel messaggio, viene eseguito l' [*hashing*](../secgloss/h-gly.md) dei dati contenuti nel messaggio, restituendo un nuovo digest.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="6a8fb-114">Confrontare il digest recuperato dal messaggio con il nuovo digest appena creato.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="6a8fb-115">Se i due digest corrispondono, la firma viene verificata.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="6a8fb-116">Ciò significa che la [*chiave privata*](../secgloss/p-gly.md) usata per firmare i dati corrisponde alla chiave pubblica appena usata per decrittografare la firma e che i dati non sono stati modificati dopo la firma dei dati.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="6a8fb-117">Se i due digest non corrispondono, la firma non viene verificata e le chiavi private/pubbliche non corrispondono oppure i dati sono stati modificati dopo la firma dei dati o entrambi.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="6a8fb-118">Una singola funzione, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), può essere usata per verificare una firma, come illustrato nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="6a8fb-119">**Per verificare un messaggio firmato**</span><span class="sxs-lookup"><span data-stu-id="6a8fb-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="6a8fb-120">Ottenere un puntatore al messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="6a8fb-121">Ottiene le dimensioni del messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="6a8fb-122">Ottenere un handle per un provider di crittografia.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="6a8fb-123">Inizializzare la struttura della [**\_ \_ \_ paragrafi di verifica del messaggio di crittografia**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) .</span><span class="sxs-lookup"><span data-stu-id="6a8fb-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="6a8fb-124">Chiamare [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) per verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="6a8fb-125">Il codice che implementa questa procedura è incluso nel [programma C di esempio: firma di un messaggio e verifica della firma di un messaggio](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="6a8fb-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
