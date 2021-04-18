---
description: I protocolli supportati e i pacchetti di crittografia possono essere elencati da chiamate a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerazione dei protocolli supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310755"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="a8d32-103">Enumerazione dei protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="a8d32-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="a8d32-104">I protocolli supportati e i pacchetti di crittografia possono essere elencati da chiamate a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex.</span><span class="sxs-lookup"><span data-stu-id="a8d32-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="a8d32-105">Il \_ valore ENUMALGS di PP \_ funziona come PP \_ ENUMALGS ma restituisce una struttura di [**prova \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) che include informazioni più dettagliate sugli algoritmi supportati dal provider.</span><span class="sxs-lookup"><span data-stu-id="a8d32-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="a8d32-106">Per ulteriori informazioni sui flag di protocollo definiti e sui relativi valori, vedere [flag di protocollo](protocol-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a8d32-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="a8d32-107">Dato che il membro **hCryptProv** è l' [*handle*](../secgloss/h-gly.md) di un [*contesto*](../secgloss/c-gly.md) di crittografia aperto acquisito usando [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) con il relativo parametro *dwProvType* impostato su prov \_ RSA \_ Schannel, nell'esempio seguente vengono elencati i nomi di tutti gli algoritmi disponibili in CSP.</span><span class="sxs-lookup"><span data-stu-id="a8d32-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



<span data-ttu-id="a8d32-108">Nella tabella seguente sono elencati alcuni algoritmi restituiti da una tipica parte interna di prove \_ RSA \_ Schannel CSP.</span><span class="sxs-lookup"><span data-stu-id="a8d32-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="a8d32-109">Si noti che in questo esempio non è supportata né la crittografia SSL2 SHA né la crittografia DES SSL2.</span><span class="sxs-lookup"><span data-stu-id="a8d32-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="a8d32-110">Identificatore dell'algoritmo</span><span class="sxs-lookup"><span data-stu-id="a8d32-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="a8d32-111">Lunghezza minima chiave</span><span class="sxs-lookup"><span data-stu-id="a8d32-111">Minimum key length</span></span> | <span data-ttu-id="a8d32-112">Lunghezza massima della chiave</span><span class="sxs-lookup"><span data-stu-id="a8d32-112">Maximum key length</span></span> | <span data-ttu-id="a8d32-113">Protocolli</span><span class="sxs-lookup"><span data-stu-id="a8d32-113">Protocols</span></span> | <span data-ttu-id="a8d32-114">Nome algoritmo</span><span class="sxs-lookup"><span data-stu-id="a8d32-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="a8d32-115">*CALG \_ RSA \_ KEYX*</span><span class="sxs-lookup"><span data-stu-id="a8d32-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="a8d32-116">512</span><span class="sxs-lookup"><span data-stu-id="a8d32-116">512</span></span>                | <span data-ttu-id="a8d32-117">2048</span><span class="sxs-lookup"><span data-stu-id="a8d32-117">2048</span></span>               | <span data-ttu-id="a8d32-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="a8d32-118">0x0007</span></span>    | <span data-ttu-id="a8d32-119">"RSA \_ KEYX"</span><span class="sxs-lookup"><span data-stu-id="a8d32-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="a8d32-120">*\_MD5 CALG*</span><span class="sxs-lookup"><span data-stu-id="a8d32-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="a8d32-121">128</span><span class="sxs-lookup"><span data-stu-id="a8d32-121">128</span></span>                | <span data-ttu-id="a8d32-122">128</span><span class="sxs-lookup"><span data-stu-id="a8d32-122">128</span></span>                | <span data-ttu-id="a8d32-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="a8d32-123">0x0007</span></span>    | <span data-ttu-id="a8d32-124">MD5</span><span class="sxs-lookup"><span data-stu-id="a8d32-124">"MD5"</span></span>          |
| [<span data-ttu-id="a8d32-125">*\_Sha CALG*</span><span class="sxs-lookup"><span data-stu-id="a8d32-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="a8d32-126">160</span><span class="sxs-lookup"><span data-stu-id="a8d32-126">160</span></span>                | <span data-ttu-id="a8d32-127">160</span><span class="sxs-lookup"><span data-stu-id="a8d32-127">160</span></span>                | <span data-ttu-id="a8d32-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="a8d32-128">0x0005</span></span>    | <span data-ttu-id="a8d32-129">Sha</span><span class="sxs-lookup"><span data-stu-id="a8d32-129">"SHA"</span></span>          |
| [<span data-ttu-id="a8d32-130">*CALG \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="a8d32-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="a8d32-131">40</span><span class="sxs-lookup"><span data-stu-id="a8d32-131">40</span></span>                 | <span data-ttu-id="a8d32-132">128</span><span class="sxs-lookup"><span data-stu-id="a8d32-132">128</span></span>                | <span data-ttu-id="a8d32-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="a8d32-133">0x0007</span></span>    | <span data-ttu-id="a8d32-134">RC4</span><span class="sxs-lookup"><span data-stu-id="a8d32-134">"RC4"</span></span>          |
| <span data-ttu-id="a8d32-135">CALG \_ des</span><span class="sxs-lookup"><span data-stu-id="a8d32-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="a8d32-136">56</span><span class="sxs-lookup"><span data-stu-id="a8d32-136">56</span></span>                 | <span data-ttu-id="a8d32-137">56</span><span class="sxs-lookup"><span data-stu-id="a8d32-137">56</span></span>                 | <span data-ttu-id="a8d32-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="a8d32-138">0x0005</span></span>    | <span data-ttu-id="a8d32-139">DES</span><span class="sxs-lookup"><span data-stu-id="a8d32-139">"DES"</span></span>          |



 

<span data-ttu-id="a8d32-140">Per preparare l'invio di messaggi ClientHello o ServerHello, il motore di protocollo [*Schannel*](../secgloss/s-gly.md) enumera gli algoritmi e le dimensioni delle chiavi supportati dal CSP e compila un elenco internamente dei pacchetti di crittografia supportati.</span><span class="sxs-lookup"><span data-stu-id="a8d32-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
