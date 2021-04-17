---
description: Attività generali necessarie per decodificare un messaggio in busta digitale.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodifica dei dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565894"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="1f1d8-103">Decodifica dei dati in busta</span><span class="sxs-lookup"><span data-stu-id="1f1d8-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="1f1d8-104">Le attività generali necessarie per decodificare un messaggio in busta digitale sono illustrate nella figura seguente e descritte nell'elenco che segue.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![decodifica dei dati in busta](images/decemsg.png)

<span data-ttu-id="1f1d8-106">La sequenza di eventi per la decodifica dei dati in busta con la gestione delle chiavi di trasporto chiave, come illustrato nella figura precedente, è la seguente:</span><span class="sxs-lookup"><span data-stu-id="1f1d8-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="1f1d8-107">Viene recuperato un puntatore al messaggio in [*busta digitale*](../secgloss/d-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1d8-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="1f1d8-108">Viene aperto un [*archivio certificati*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1d8-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="1f1d8-109">Dal messaggio, viene recuperato l'ID del destinatario (ID).</span><span class="sxs-lookup"><span data-stu-id="1f1d8-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="1f1d8-110">L'ID del destinatario viene usato per recuperare il certificato.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="1f1d8-111">Viene recuperata la [*chiave privata*](../secgloss/p-gly.md) associata al certificato.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="1f1d8-112">La chiave privata viene utilizzata per decrittografare la chiave [*simmetrica*](../secgloss/s-gly.md) ([*sessione*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="1f1d8-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="1f1d8-113">L'algoritmo di crittografia viene recuperato dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="1f1d8-114">Utilizzando la chiave privata e l'algoritmo di crittografia, i dati vengono decrittografati.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="1f1d8-115">Nella procedura seguente vengono utilizzate le funzioni di messaggio di basso livello per eseguire le attività elencate.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="1f1d8-116">**Per decodificare un messaggio in busta digitale**</span><span class="sxs-lookup"><span data-stu-id="1f1d8-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="1f1d8-117">Ottenere un puntatore al BLOB codificato.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="1f1d8-118">Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="1f1d8-119">Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati che devono essere decodificati.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="1f1d8-120">In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="1f1d8-121">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 2 e CMSG \_ di tipo \_ param per verificare che il messaggio sia del tipo di dati con envelope.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="1f1d8-122">Chiamare di nuovo [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando \_ il parametro del tipo di contenuto interno CMSG \_ \_ \_ per ottenere il tipo di dati del [*contenuto interno*](../secgloss/i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1f1d8-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="1f1d8-123">Se il tipo di dati del contenuto interno è **dati**, continuare a decrittografare e decodificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="1f1d8-124">In caso contrario, eseguire una procedura di decodifica appropriata per il tipo di dati content.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="1f1d8-125">Supponendo che il tipo di contenuto interno sia "data", inizializzare la struttura [**CMSG \_ CTRL \_ Decrypt \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data e chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CMSG \_ CTRL \_ Decrypt e l'indirizzo della struttura.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="1f1d8-126">Il contenuto verrà decrittografato.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="1f1d8-127">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando \_ il parametro di contenuto CMSG \_ per ottenere un puntatore al BLOB di dati del contenuto decodificato (stringa di **byte** ).</span><span class="sxs-lookup"><span data-stu-id="1f1d8-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="1f1d8-128">Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="1f1d8-129">Il risultato di questa procedura è che il messaggio viene decodificato e decrittografato e viene recuperato un puntatore al BLOB di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="1f1d8-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f1d8-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f1d8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f1d8-131">Esempio di programma C: codifica di un messaggio firmato in busta</span><span class="sxs-lookup"><span data-stu-id="1f1d8-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
