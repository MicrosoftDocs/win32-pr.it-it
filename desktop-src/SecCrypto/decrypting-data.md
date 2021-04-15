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
# <a name="decrypting-data"></a><span data-ttu-id="1e197-103">Decrittografia di dati</span><span class="sxs-lookup"><span data-stu-id="1e197-103">Decrypting Data</span></span>

<span data-ttu-id="1e197-104">In questa sezione vengono illustrati i passaggi per decrittografare un messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="1e197-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="1e197-105">**Per decrittografare un messaggio crittografato**</span><span class="sxs-lookup"><span data-stu-id="1e197-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="1e197-106">Ottenere un puntatore al messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="1e197-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="1e197-107">Aprire un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="1e197-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="1e197-108">Dal messaggio recuperare l'identificatore del destinatario (ID).</span><span class="sxs-lookup"><span data-stu-id="1e197-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="1e197-109">Utilizzare l'identificatore del destinatario per recuperare il certificato.</span><span class="sxs-lookup"><span data-stu-id="1e197-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="1e197-110">Ottenere la chiave privata per il certificato.</span><span class="sxs-lookup"><span data-stu-id="1e197-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="1e197-111">Utilizzare la chiave privata per decrittografare la chiave simmetrica (sessione).</span><span class="sxs-lookup"><span data-stu-id="1e197-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="1e197-112">Recuperare l'algoritmo di crittografia dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e197-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="1e197-113">Utilizzando la chiave della sessione decrittografata e l'algoritmo di crittografia, decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="1e197-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="1e197-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) esegue tutte le attività per la decrittografia di un messaggio. Tuttavia, l'inizializzazione di strutture e altri dati è ancora necessaria.</span><span class="sxs-lookup"><span data-stu-id="1e197-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="1e197-115">**Per decrittografare i dati tramite CryptDecryptMessage**</span><span class="sxs-lookup"><span data-stu-id="1e197-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="1e197-116">Ottenere un puntatore al BLOB crittografato.</span><span class="sxs-lookup"><span data-stu-id="1e197-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="1e197-117">Aprire un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="1e197-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="1e197-118">Creare una matrice dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="1e197-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="1e197-119">Inizializzare la struttura [**\_ paracrypt \_ message \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) paracrypt.</span><span class="sxs-lookup"><span data-stu-id="1e197-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="1e197-120">Chiamare [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per decrittografare i dati contenuti nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="1e197-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="1e197-121">[Esempio di programma C: l'utilizzo di CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa la procedura appena presentata.</span><span class="sxs-lookup"><span data-stu-id="1e197-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="1e197-122">I commenti mostrano gli elementi di codice che eseguono ogni passaggio della procedura.</span><span class="sxs-lookup"><span data-stu-id="1e197-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="1e197-123">Per informazioni dettagliate sulla funzione, vedere [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)e per informazioni dettagliate sulla struttura dei dati, vedere [**crypt \_ Decrypt \_ message \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span><span class="sxs-lookup"><span data-stu-id="1e197-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 



