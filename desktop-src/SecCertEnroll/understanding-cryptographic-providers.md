---
description: I provider implementano gli algoritmi di crittografia, generano chiavi, forniscono archiviazione chiavi e autenticano gli utenti. I provider possono essere implementati in hardware, software o entrambi.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Informazioni sui provider di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968062"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="3c72f-104">Informazioni sui provider di crittografia</span><span class="sxs-lookup"><span data-stu-id="3c72f-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="3c72f-105">Il concetto di provider del servizio di crittografia introdotto nell'API di crittografia ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) e che si è evoluto in qualche modo nell' [*API di crittografia: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) è fondamentale per l'implementazione sicura della funzionalità di crittografia nei sistemi operativi Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c72f-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="3c72f-106">Questi due SDK sono stati usati per creare molte applicazioni e vengono chiamati internamente da altri SDK.</span><span class="sxs-lookup"><span data-stu-id="3c72f-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="3c72f-107">Ad esempio, Active Directory Servizi certificati e l'API di registrazione certificati si basano su CryptoAPI e CNG.</span><span class="sxs-lookup"><span data-stu-id="3c72f-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="3c72f-108">In generale, i provider implementano gli algoritmi di crittografia, generano chiavi, forniscono archiviazione chiavi e autenticano gli utenti.</span><span class="sxs-lookup"><span data-stu-id="3c72f-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="3c72f-109">I provider possono essere implementati in hardware, software o entrambi.</span><span class="sxs-lookup"><span data-stu-id="3c72f-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="3c72f-110">Le applicazioni compilate tramite CryptoAPI o CNG non possono modificare le chiavi create dai provider e non possono modificare l'implementazione dell'algoritmo crittografico.</span><span class="sxs-lookup"><span data-stu-id="3c72f-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="3c72f-111">I provider multipli creati da Microsoft vengono distribuiti con i sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="3c72f-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="3c72f-112">Altri provider sono stati creati e distribuiti da terze parti.</span><span class="sxs-lookup"><span data-stu-id="3c72f-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="3c72f-113">Negli argomenti seguenti vengono evidenziate le differenze tra i provider associati a CryptoAPI e quelli associati a CNG.</span><span class="sxs-lookup"><span data-stu-id="3c72f-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="3c72f-114">Questa documentazione si riferisce in genere a provider senza riferimento all'SDK a cui sono associati, annotando l'associazione solo quando è pertinente.</span><span class="sxs-lookup"><span data-stu-id="3c72f-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="3c72f-115">Provider del servizio di crittografia CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="3c72f-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="3c72f-116">Provider di algoritmi di crittografia CNG</span><span class="sxs-lookup"><span data-stu-id="3c72f-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="3c72f-117">Provider di archiviazione chiavi CNG</span><span class="sxs-lookup"><span data-stu-id="3c72f-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="3c72f-118">Enumerazione dei provider installati</span><span class="sxs-lookup"><span data-stu-id="3c72f-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="3c72f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c72f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c72f-120">Uso dell'API di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="3c72f-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
