---
description: Microsoft Enhanced Cryptographic Provider fornisce un'applicazione con una sicurezza più avanzata rispetto a quella attualmente disponibile con il provider di crittografia di base Microsoft. Una maggiore lunghezza della chiave offre agli utenti maggiore protezione per i dati sensibili.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Confronto Lunghezza chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885657"
---
# <a name="key-length-comparison"></a><span data-ttu-id="53199-104">Confronto Lunghezza chiave</span><span class="sxs-lookup"><span data-stu-id="53199-104">Key Length Comparison</span></span>

<span data-ttu-id="53199-105">Microsoft Enhanced Cryptographic Provider fornisce un'applicazione con una sicurezza più avanzata rispetto a quella attualmente disponibile con il provider di crittografia di base Microsoft.</span><span class="sxs-lookup"><span data-stu-id="53199-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="53199-106">Una maggiore lunghezza della chiave offre agli utenti maggiore protezione per i dati sensibili.</span><span class="sxs-lookup"><span data-stu-id="53199-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="53199-107">La tabella seguente elenca le [*lunghezze di chiave*](../secgloss/k-gly.md) predefinite supportate dal provider di base e il provider avanzato per gli algoritmi standard.</span><span class="sxs-lookup"><span data-stu-id="53199-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="53199-108">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="53199-108">Algorithm</span></span>                                                                                | <span data-ttu-id="53199-109">Provider di base</span><span class="sxs-lookup"><span data-stu-id="53199-109">Base Provider</span></span> | <span data-ttu-id="53199-110">Provider avanzati e avanzati</span><span class="sxs-lookup"><span data-stu-id="53199-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="53199-111">Scambio di chiavi RSA</span><span class="sxs-lookup"><span data-stu-id="53199-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="53199-112">512 bit</span><span class="sxs-lookup"><span data-stu-id="53199-112">512-bit</span></span>       | <span data-ttu-id="53199-113">1.024 bit</span><span class="sxs-lookup"><span data-stu-id="53199-113">1,024-bit</span></span>                     |
| <span data-ttu-id="53199-114">Firma RSA</span><span class="sxs-lookup"><span data-stu-id="53199-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="53199-115">512 bit</span><span class="sxs-lookup"><span data-stu-id="53199-115">512-bit</span></span>       | <span data-ttu-id="53199-116">1.024 bit</span><span class="sxs-lookup"><span data-stu-id="53199-116">1,024-bit</span></span>                     |
| <span data-ttu-id="53199-117">RC2</span><span class="sxs-lookup"><span data-stu-id="53199-117">RC2</span></span>                                                                                      | <span data-ttu-id="53199-118">40 bit</span><span class="sxs-lookup"><span data-stu-id="53199-118">40-bit</span></span>        | <span data-ttu-id="53199-119">128 bit</span><span class="sxs-lookup"><span data-stu-id="53199-119">128-bit</span></span>                       |
| <span data-ttu-id="53199-120">RC4</span><span class="sxs-lookup"><span data-stu-id="53199-120">RC4</span></span>                                                                                      | <span data-ttu-id="53199-121">40 bit</span><span class="sxs-lookup"><span data-stu-id="53199-121">40-bit</span></span>        | <span data-ttu-id="53199-122">128 bit</span><span class="sxs-lookup"><span data-stu-id="53199-122">128-bit</span></span>                       |
| <span data-ttu-id="53199-123">DES</span><span class="sxs-lookup"><span data-stu-id="53199-123">DES</span></span>                                                                                      | <span data-ttu-id="53199-124">Non supportato</span><span class="sxs-lookup"><span data-stu-id="53199-124">Not supported</span></span> | <span data-ttu-id="53199-125">56 bit</span><span class="sxs-lookup"><span data-stu-id="53199-125">56-bit</span></span>                        |
| <span data-ttu-id="53199-126">[*Triple des*](../secgloss/t-gly.md) (2 chiavi)</span><span class="sxs-lookup"><span data-stu-id="53199-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="53199-127">Non supportato</span><span class="sxs-lookup"><span data-stu-id="53199-127">Not supported</span></span> | <span data-ttu-id="53199-128">112 bit</span><span class="sxs-lookup"><span data-stu-id="53199-128">112-bit</span></span>                       |
| <span data-ttu-id="53199-129">Triple DES (3 chiavi)</span><span class="sxs-lookup"><span data-stu-id="53199-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="53199-130">Non supportato</span><span class="sxs-lookup"><span data-stu-id="53199-130">Not supported</span></span> | <span data-ttu-id="53199-131">168 bit</span><span class="sxs-lookup"><span data-stu-id="53199-131">168-bit</span></span>                       |



 

<span data-ttu-id="53199-132">Gli algoritmi [*des e*](../secgloss/d-gly.md) [*triple des*](../secgloss/t-gly.md) sono supportati nel provider migliorato.</span><span class="sxs-lookup"><span data-stu-id="53199-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="53199-133">Il provider avanzato è compatibile con le versioni precedenti del provider di base distribuito con le versioni precedenti di CryptoAPI con la seguente eccezione.</span><span class="sxs-lookup"><span data-stu-id="53199-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="53199-134">Sia il provider di base che il provider avanzato possono generare solo chiavi di sessione con la lunghezza della chiave predefinita.</span><span class="sxs-lookup"><span data-stu-id="53199-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="53199-135">La lunghezza predefinita delle chiavi di sessione per il provider di base è 40 bit.</span><span class="sxs-lookup"><span data-stu-id="53199-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="53199-136">La lunghezza della chiave predefinita per il provider avanzato è 128 bit.</span><span class="sxs-lookup"><span data-stu-id="53199-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="53199-137">Il provider avanzato non può creare chiavi con lunghezze di chiave compatibili con il provider di base.</span><span class="sxs-lookup"><span data-stu-id="53199-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="53199-138">Tuttavia, il provider avanzato può importare lunghezze di chiave di qualsiasi dimensione, fino a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="53199-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
