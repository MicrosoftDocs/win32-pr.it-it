---
description: Processo per decodificare i dati firmati.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodifica dei dati firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306443"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="7247f-103">Decodifica dei dati firmati</span><span class="sxs-lookup"><span data-stu-id="7247f-103">Decoding Signed Data</span></span>

<span data-ttu-id="7247f-104">Il processo generale seguente decodifica un tipo di [*dati con segno*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7247f-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="7247f-105">**Per decodificare un messaggio firmato**</span><span class="sxs-lookup"><span data-stu-id="7247f-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="7247f-106">Ottenere un puntatore al BLOB codificato.</span><span class="sxs-lookup"><span data-stu-id="7247f-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="7247f-107">Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari.</span><span class="sxs-lookup"><span data-stu-id="7247f-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="7247f-108">Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati che devono essere decodificati.</span><span class="sxs-lookup"><span data-stu-id="7247f-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="7247f-109">In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="7247f-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="7247f-110">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 2 e i tipi di parametro appropriati per accedere ai dati decodificati.</span><span class="sxs-lookup"><span data-stu-id="7247f-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="7247f-111">Ad esempio, passare CMSG \_ Content \_ param per ottenere un puntatore al contenuto decodificato.</span><span class="sxs-lookup"><span data-stu-id="7247f-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="7247f-112">Nel processo generale seguente viene verificata la firma di un messaggio firmato decodificato.</span><span class="sxs-lookup"><span data-stu-id="7247f-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="7247f-113">**Per verificare la firma di un messaggio firmato decodificato**</span><span class="sxs-lookup"><span data-stu-id="7247f-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="7247f-114">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando le informazioni sul certificato del firmatario e sull'handle del messaggio CMSG \_ \_ \_ \_ per ottenere le [**\_ informazioni sul certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmatario dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="7247f-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="7247f-115">Chiamare [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) per aprire un archivio temporaneo inizializzato con i certificati del messaggio.</span><span class="sxs-lookup"><span data-stu-id="7247f-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="7247f-116">Chiamare [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) per ottenere le [**\_ informazioni sul certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmatario dai certificati inclusi nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="7247f-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="7247f-117">Chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando il CMSG \_ CTRL \_ Verify \_ Signature per verificare le firme.</span><span class="sxs-lookup"><span data-stu-id="7247f-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="7247f-118">Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7247f-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="7247f-119">Il risultato di queste procedure è che la firma viene verificata e un puntatore viene recuperato al contenuto del messaggio decodificato ottenuto nel passaggio 4 della procedura per la decodifica di un messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="7247f-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="7247f-120">Per informazioni sul codice C, vedere [esempio di programma c: firma, codifica, decodifica e verifica di un messaggio](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="7247f-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
