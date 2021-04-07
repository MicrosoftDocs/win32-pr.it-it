---
description: Supporta le firme digitali e la crittografia dei dati. Viene considerato un provider del servizio di crittografia (CSP) per utilizzo generico.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057962"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="c7fd1-104">PROVA \_ \_ AES RSA</span><span class="sxs-lookup"><span data-stu-id="c7fd1-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="c7fd1-105">Il \_ tipo di \_ provider AES RSA di prova supporta sia le [firme digitali](digital-signatures.md) sia la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="c7fd1-106">Viene considerato un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="c7fd1-107">L' [*algoritmo di chiave pubblica*](../secgloss/p-gly.md) RSA viene utilizzato per tutte le operazioni con [*chiave pubblica*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7fd1-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="c7fd1-108">Algoritmi supportati</span><span class="sxs-lookup"><span data-stu-id="c7fd1-108">Algorithms Supported</span></span>

<span data-ttu-id="c7fd1-109">Per le descrizioni di ognuno di questi algoritmi, vedere il glossario.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="c7fd1-110">Scopo</span><span class="sxs-lookup"><span data-stu-id="c7fd1-110">Purpose</span></span>      | <span data-ttu-id="c7fd1-111">Algoritmi supportati</span><span class="sxs-lookup"><span data-stu-id="c7fd1-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fd1-112">Scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="c7fd1-112">Key Exchange</span></span> | [<span data-ttu-id="c7fd1-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="c7fd1-114">Firma</span><span class="sxs-lookup"><span data-stu-id="c7fd1-114">Signature</span></span>    | [<span data-ttu-id="c7fd1-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="c7fd1-116">Crittografia</span><span class="sxs-lookup"><span data-stu-id="c7fd1-116">Encryption</span></span>   | [<span data-ttu-id="c7fd1-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="c7fd1-118">*RC4*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="c7fd1-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span><span class="sxs-lookup"><span data-stu-id="c7fd1-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="c7fd1-120">Hashing</span><span class="sxs-lookup"><span data-stu-id="c7fd1-120">Hashing</span></span>      | [<span data-ttu-id="c7fd1-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="c7fd1-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="c7fd1-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="c7fd1-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="c7fd1-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="c7fd1-125">SHA-2 (SHA-256, SHA-384 e SHA-512)</span><span class="sxs-lookup"><span data-stu-id="c7fd1-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="c7fd1-126">Related Documentation (Documentazione correlata)</span><span class="sxs-lookup"><span data-stu-id="c7fd1-126">Related Documentation</span></span>

<span data-ttu-id="c7fd1-127">Questo tipo di provider è definito da Microsoft e dalla sicurezza dei dati RSA.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="c7fd1-128">Viene descritto nei documenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c7fd1-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="c7fd1-129">*Guida per programmatori del provider del servizio di crittografia Microsoft*, microsoft, 1996.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="c7fd1-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="c7fd1-131">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="c7fd1-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 
