---
title: Servizi di base TPM
description: Il software TPM fornisce servizi come API esposte tramite Remote Procedure Call. Utilizzare TPM per creare un modulo TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- Servizi di base TPM TBS
- Servizi di base TPM TBS, home page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399390"
---
# <a name="tpm-base-services"></a><span data-ttu-id="93225-106">Servizi di base TPM</span><span class="sxs-lookup"><span data-stu-id="93225-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="93225-107">Scopo</span><span class="sxs-lookup"><span data-stu-id="93225-107">Purpose</span></span>

<span data-ttu-id="93225-108">La funzionalità dei servizi di base Trusted Platform Module (TPM) centralizza l'accesso TPM tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="93225-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="93225-109">La funzionalità TBS viene eseguita come servizio di sistema in Windows Server 2008, Windows Vista o sistemi operativi più recenti.</span><span class="sxs-lookup"><span data-stu-id="93225-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="93225-110">Fornisce servizi come API esposte tramite RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="93225-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="93225-111">La funzionalità TBS usa le priorità specificate chiamando le applicazioni per pianificare in modo cooperativo l'accesso a TPM.</span><span class="sxs-lookup"><span data-stu-id="93225-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="93225-112">Il TPM può essere usato per le operazioni di archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="93225-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="93225-113">Tuttavia, gli sviluppatori sono invitati a utilizzare le [API di archiviazione chiavi](/windows/desktop/SecCNG/key-storage-and-retrieval) per questi scenari.</span><span class="sxs-lookup"><span data-stu-id="93225-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="93225-114">Le API di archiviazione chiavi forniscono la funzionalità per creare, firmare o crittografare con e rendere permanente le chiavi crittografiche e sono di livello superiore e più semplice da usare rispetto a TBS per questi scenari di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93225-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="93225-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="93225-115">Developer audience</span></span>

<span data-ttu-id="93225-116">TBS è progettato per l'uso da parte di sviluppatori di applicazioni basate sui sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="93225-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="93225-117">Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="93225-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="93225-118">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="93225-118">Run-time requirements</span></span>

<span data-ttu-id="93225-119">La funzionalità TBS richiede almeno Windows Server 2008 o sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="93225-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="93225-120">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="93225-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="93225-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="93225-121">In this section</span></span>



| <span data-ttu-id="93225-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="93225-122">Topic</span></span>                                         | <span data-ttu-id="93225-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93225-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="93225-124">Informazioni su TBS</span><span class="sxs-lookup"><span data-stu-id="93225-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="93225-125">Concetti chiave e una visualizzazione di alto livello della funzionalità TBS.</span><span class="sxs-lookup"><span data-stu-id="93225-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="93225-126">Uso di TBS</span><span class="sxs-lookup"><span data-stu-id="93225-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="93225-127">Processi e procedure di TBS per l'uso dell'API TBS.</span><span class="sxs-lookup"><span data-stu-id="93225-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="93225-128">Riferimento a TBS</span><span class="sxs-lookup"><span data-stu-id="93225-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="93225-129">Documentazione sulle funzioni, le strutture e i codici restituiti di TBS.</span><span class="sxs-lookup"><span data-stu-id="93225-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

