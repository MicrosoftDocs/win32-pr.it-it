---
description: Descrive le attività che devono essere eseguite per creare un messaggio firmato.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Creazione di un messaggio firmato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232219"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="1bd42-103">Creazione di un messaggio firmato</span><span class="sxs-lookup"><span data-stu-id="1bd42-103">Creating a Signed Message</span></span>

<span data-ttu-id="1bd42-104">Nella figura seguente vengono illustrate le attività che devono essere eseguite per creare un messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="1bd42-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="1bd42-105">I passaggi sono elencati dopo l'illustrazione.</span><span class="sxs-lookup"><span data-stu-id="1bd42-105">The steps are listed following the illustration.</span></span>

![firma di un messaggio](images/signdmsg.png)

<span data-ttu-id="1bd42-107">**Per creare un messaggio firmato**</span><span class="sxs-lookup"><span data-stu-id="1bd42-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="1bd42-108">Creare i dati (se necessario) e ottenere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="1bd42-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="1bd42-109">Aprire un [*archivio certificati*](../secgloss/c-gly.md) che contiene il certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="1bd42-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="1bd42-110">Ottenere la [*chiave privata*](../secgloss/p-gly.md) per il certificato.</span><span class="sxs-lookup"><span data-stu-id="1bd42-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="1bd42-111">Una proprietà deve essere impostata sul certificato prima di utilizzarla, per associare un certificato a un particolare [*CSP*](../secgloss/c-gly.md)e, all'interno di tale CSP, a una chiave privata specifica.</span><span class="sxs-lookup"><span data-stu-id="1bd42-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="1bd42-112">Questa operazione deve essere impostata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="1bd42-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="1bd42-113">Scegliere un algoritmo di hash per l'operazione digest.</span><span class="sxs-lookup"><span data-stu-id="1bd42-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="1bd42-114">Si consiglia di selezionare l'algoritmo hash da un percorso configurabile che può essere successivamente aggiornato senza richiedere modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="1bd42-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="1bd42-115">Inviare i dati tramite la funzione hash usando l'algoritmo hash, creando in tal modo un [*hash*](../secgloss/h-gly.md) (digest) dei dati.</span><span class="sxs-lookup"><span data-stu-id="1bd42-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="1bd42-116">Utilizzando la [*chiave privata*](../secgloss/p-gly.md) ottenuta tramite la proprietà del certificato, crittografare il digest e creare la firma.</span><span class="sxs-lookup"><span data-stu-id="1bd42-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="1bd42-117">Includere quanto segue nel messaggio firmato:</span><span class="sxs-lookup"><span data-stu-id="1bd42-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="1bd42-118">Dati firmati</span><span class="sxs-lookup"><span data-stu-id="1bd42-118">The signed data</span></span>
    -   <span data-ttu-id="1bd42-119">Algoritmo hash</span><span class="sxs-lookup"><span data-stu-id="1bd42-119">The hash algorithm</span></span>
    -   <span data-ttu-id="1bd42-120">Firma</span><span class="sxs-lookup"><span data-stu-id="1bd42-120">The signature</span></span>
    -   <span data-ttu-id="1bd42-121">Identificatore del firmatario (autorità emittente del certificato e numero di serie)</span><span class="sxs-lookup"><span data-stu-id="1bd42-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="1bd42-122">Il certificato del firmatario (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="1bd42-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="1bd42-123">Per una procedura dettagliata e un esempio, vedere la [procedura per la firma di dati](procedure-for-signing-data.md) e [il programma C di esempio: firma di un messaggio e verifica della firma di un messaggio](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="1bd42-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
