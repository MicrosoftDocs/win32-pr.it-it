---
description: Importante questa API è deprecata.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401653"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="b8cd9-103">Provider del servizio di crittografia</span><span class="sxs-lookup"><span data-stu-id="b8cd9-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8cd9-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-104">This API is deprecated.</span></span> <span data-ttu-id="b8cd9-105">Il software nuovo ed esistente dovrebbe iniziare a usare le [API di prossima generazione di crittografia.](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="b8cd9-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="b8cd9-106">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="b8cd9-107">Un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) contiene implementazioni di algoritmi e standard crittografici.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="b8cd9-108">Come minimo, un CSP è costituito da una [*libreria di collegamento dinamico*](../secgloss/d-gly.md) (dll) che implementa le funzioni in [*CryptoSPI*](../secgloss/c-gly.md) (un'interfaccia del [*programma di sistema*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="b8cd9-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="b8cd9-109">La maggior parte dei CSP contiene l'implementazione di tutte le relative funzioni.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="b8cd9-110">Alcuni CSP, tuttavia, implementano le proprie funzioni principalmente in un programma di servizio basato su Windows gestito da Gestione controllo servizi di Windows.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="b8cd9-111">Altri implementano funzioni in hardware, ad esempio una [*Smart Card*](../secgloss/s-gly.md) o un coprocessore protetto.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="b8cd9-112">Se un CSP non implementa funzioni proprie, la DLL funge da livello pass-through, facilitando la comunicazione tra il sistema operativo e l'implementazione effettiva di CSP.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="b8cd9-113">Questa sezione include gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-113">This section includes the following topics.</span></span>



| <span data-ttu-id="b8cd9-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="b8cd9-114">Topic</span></span>                                                                                      | <span data-ttu-id="b8cd9-115">Contenuto</span><span class="sxs-lookup"><span data-stu-id="b8cd9-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8cd9-116">Tipi di provider di crittografia</span><span class="sxs-lookup"><span data-stu-id="b8cd9-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="b8cd9-117">I tipi di provider del servizio di crittografia sono famiglie di provider di servizi di crittografia che condividono formati di dati e protocolli crittografici.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="b8cd9-118">I formati di dati includono schemi di [*riempimento*](../secgloss/p-gly.md) degli algoritmi, [*lunghezze delle chiavi*](../secgloss/k-gly.md)e modalità predefinite.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="b8cd9-119">Provider del servizio di crittografia Microsoft</span><span class="sxs-lookup"><span data-stu-id="b8cd9-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="b8cd9-120">Informazioni dettagliate sui CSP attualmente disponibili da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8cd9-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
