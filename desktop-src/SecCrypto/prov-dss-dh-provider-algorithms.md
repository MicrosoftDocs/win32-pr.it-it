---
description: Algoritmi supportati da Microsoft Base DSS e Diffie-Hellman provider di crittografia.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algoritmi del provider di PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319350"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="4ae73-103">Prove \_ del \_ provider DH di prova DSS</span><span class="sxs-lookup"><span data-stu-id="4ae73-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="4ae73-104">Nella tabella seguente sono elencati gli algoritmi supportati da Microsoft Base DSS e Diffie-Hellman provider di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4ae73-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="4ae73-105">ID algoritmo</span><span class="sxs-lookup"><span data-stu-id="4ae73-105">Algorithm ID</span></span>      | <span data-ttu-id="4ae73-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ae73-106">Description</span></span>                                 | <span data-ttu-id="4ae73-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ae73-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae73-108">\_MD5 CALG</span><span class="sxs-lookup"><span data-stu-id="4ae73-108">CALG\_MD5</span></span>         | <span data-ttu-id="4ae73-109">Algoritmo di hash MD5.</span><span class="sxs-lookup"><span data-stu-id="4ae73-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="4ae73-110">Fornito solo per l'hashing.</span><span class="sxs-lookup"><span data-stu-id="4ae73-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="4ae73-111">\_Sha CALG</span><span class="sxs-lookup"><span data-stu-id="4ae73-111">CALG\_SHA</span></span>         | <span data-ttu-id="4ae73-112">Algoritmo di hash SHA.</span><span class="sxs-lookup"><span data-stu-id="4ae73-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="4ae73-113">Deve essere usato per le firme DSS.</span><span class="sxs-lookup"><span data-stu-id="4ae73-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="4ae73-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="4ae73-114">CALG\_SHA1</span></span>        | <span data-ttu-id="4ae73-115">Uguale a CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="4ae73-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="4ae73-116">Nessun commento.</span><span class="sxs-lookup"><span data-stu-id="4ae73-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="4ae73-117">\_firma CALG DSS \_</span><span class="sxs-lookup"><span data-stu-id="4ae73-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="4ae73-118">Algoritmo di firma della chiave pubblica/privata DSS.</span><span class="sxs-lookup"><span data-stu-id="4ae73-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="4ae73-119">Lunghezza della chiave: è possibile impostare 512 bit su 1.024 bit in incrementi di 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="4ae73-120">Lunghezza chiave predefinita: 1.024 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="4ae73-121">CALG \_ DH \_ SF</span><span class="sxs-lookup"><span data-stu-id="4ae73-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="4ae73-122">Archiviare e trasmettere lo scambio delle chiavi D-H.</span><span class="sxs-lookup"><span data-stu-id="4ae73-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="4ae73-123">Lunghezza della chiave: è possibile impostare 384 bit su 512 bit in incrementi di 8 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="4ae73-124">Lunghezza chiave predefinita: 512 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="4ae73-125">CALG \_ DH \_ EPHEM</span><span class="sxs-lookup"><span data-stu-id="4ae73-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="4ae73-126">Scambio di chiavi temporaneo D-H.</span><span class="sxs-lookup"><span data-stu-id="4ae73-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="4ae73-127">Lunghezza della chiave: è possibile impostare 384 bit su 512 bit in incrementi di 8 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="4ae73-128">Lunghezza chiave predefinita: 512 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="4ae73-129">CALG \_ CYLINK \_ MEK</span><span class="sxs-lookup"><span data-stu-id="4ae73-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="4ae73-130">Variante a 40 bit di una chiave DES.</span><span class="sxs-lookup"><span data-stu-id="4ae73-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="4ae73-131">Lunghezza della chiave: 40 bit.</span><span class="sxs-lookup"><span data-stu-id="4ae73-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




