---
description: Il futuro della crittografia e delle comunicazioni sicure non può essere facilmente stimato.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Estensione della funzionalità CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968452"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="242c3-103">Estensione della funzionalità CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="242c3-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="242c3-104">Il futuro della [*crittografia*](../secgloss/c-gly.md) e delle comunicazioni sicure non può essere facilmente stimato.</span><span class="sxs-lookup"><span data-stu-id="242c3-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="242c3-105">Potrebbero emergere nuovi tipi di certificato, diverse estensioni di certificato possono trovare l'utilizzo comune e i nuovi tipi di messaggio potrebbero essere introdotti.</span><span class="sxs-lookup"><span data-stu-id="242c3-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="242c3-106">Per questo motivo, l'estendibilità è parte della progettazione delle funzioni [*CryptoAPI*](../secgloss/c-gly.md) chiave.</span><span class="sxs-lookup"><span data-stu-id="242c3-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="242c3-107">Le sezioni seguenti presentano panoramiche sull'uso di OID per l'estensione delle funzioni CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="242c3-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="242c3-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="242c3-108">Topic</span></span>                                                                              | <span data-ttu-id="242c3-109">Contenuto</span><span class="sxs-lookup"><span data-stu-id="242c3-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="242c3-110">Panoramica di OID</span><span class="sxs-lookup"><span data-stu-id="242c3-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="242c3-111">Concetti fondamentali di OID.</span><span class="sxs-lookup"><span data-stu-id="242c3-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="242c3-112">Creazione della nuova funzionalità</span><span class="sxs-lookup"><span data-stu-id="242c3-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="242c3-113">Creazione di OID e funzioni per estendere l'uso delle API esistenti.</span><span class="sxs-lookup"><span data-stu-id="242c3-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="242c3-114">Registrazione della nuova funzionalità</span><span class="sxs-lookup"><span data-stu-id="242c3-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="242c3-115">Impostazione delle nuove funzioni correlate a OID.</span><span class="sxs-lookup"><span data-stu-id="242c3-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="242c3-116">Installazione della nuova funzionalità</span><span class="sxs-lookup"><span data-stu-id="242c3-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="242c3-117">Installazione di funzioni OID in memoria per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="242c3-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="242c3-118">Estensione della funzionalità CertOpenStore</span><span class="sxs-lookup"><span data-stu-id="242c3-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="242c3-119">Estensione della funzionalità [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) tramite la funzione Installable o Certificate-Store-provider Certificate.</span><span class="sxs-lookup"><span data-stu-id="242c3-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
