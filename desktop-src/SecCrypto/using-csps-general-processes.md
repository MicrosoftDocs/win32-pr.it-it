---
description: Quando si usano i provider del servizio di crittografia CSP, tenere presenti le convenzioni seguenti.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Uso dei CSP: processi generali'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308635"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="f61b8-103">Uso dei CSP: processi generali</span><span class="sxs-lookup"><span data-stu-id="f61b8-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="f61b8-104">Quando si usano i [*provider del servizio di crittografia*](../secgloss/c-gly.md) CSP, tenere presenti le convenzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f61b8-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="f61b8-105">Caching della chiave privata</span><span class="sxs-lookup"><span data-stu-id="f61b8-105">Private Key Caching</span></span>

<span data-ttu-id="f61b8-106">Un CSP può memorizzare nella cache alcune [*chiavi private*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f61b8-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="f61b8-107">È possibile controllare la memorizzazione nella cache della chiave privata in un livello globale, ma non in base all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f61b8-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="f61b8-108">Le modifiche di Caching vengono apportate modificando determinate impostazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f61b8-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="f61b8-109">Per altre informazioni, vedere [**costanti di caching della chiave privata**](private-key-caching-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f61b8-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="f61b8-110">Convenzioni del codice di esempio</span><span class="sxs-lookup"><span data-stu-id="f61b8-110">Example Code Conventions</span></span>

<span data-ttu-id="f61b8-111">Per fornire codice più conciso e leggibile, alcuni principi di buone procedure di programmazione non sono sempre seguiti negli esempi.</span><span class="sxs-lookup"><span data-stu-id="f61b8-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="f61b8-112">In particolare:</span><span class="sxs-lookup"><span data-stu-id="f61b8-112">In particular:</span></span>

-   <span data-ttu-id="f61b8-113">Vengono visualizzate solo le risposte di errore limitate.</span><span class="sxs-lookup"><span data-stu-id="f61b8-113">Only limited error responses are shown.</span></span> <span data-ttu-id="f61b8-114">I programmi ben scritti e completi controllano i codici di errore restituiti ed eseguono le azioni appropriate quando viene rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="f61b8-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="f61b8-115">Viene eseguita solo la memoria limitata e la gestione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f61b8-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="f61b8-116">Programmi ben scritti e completi eliminano tutte le chiavi e gli [*hash*](../secgloss/h-gly.md), liberano tutta la memoria allocata, chiudono tutti i file e rilasciano tutti gli handle.</span><span class="sxs-lookup"><span data-stu-id="f61b8-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="f61b8-117">Questi esempi forniscono solo dimostrazioni limitate dell'utilizzo di funzioni che eseguono queste attività.</span><span class="sxs-lookup"><span data-stu-id="f61b8-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="f61b8-118">Questi esempi non eseguono attività di memoria o di gestione delle risorse in caso di interruzione del programma a causa di errori.</span><span class="sxs-lookup"><span data-stu-id="f61b8-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="f61b8-119">Negli argomenti seguenti vengono presentate informazioni generali sugli esempi di procedure, oltre a codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="f61b8-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="f61b8-120">Recupero di dati di lunghezza sconosciuta</span><span class="sxs-lookup"><span data-stu-id="f61b8-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="f61b8-121">Enumerazione dei protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="f61b8-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
