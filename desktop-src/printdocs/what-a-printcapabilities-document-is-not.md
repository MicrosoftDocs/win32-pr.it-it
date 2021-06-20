---
description: Informazioni su alcune funzionalità e informazioni che il documento PrintCapabilities non è destinato a fornire.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Cosa non è un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409894"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="c8fa0-103">Cosa non è un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c8fa0-103">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="c8fa0-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-104">This topic is not current.</span></span> <span data-ttu-id="c8fa0-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c8fa0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c8fa0-106">È opportuno elencare alcune delle funzionalità e delle informazioni che il documento PrintCapabilities non è destinato a fornire.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-106">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="c8fa0-107">Un documento PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="c8fa0-107">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="c8fa0-108">Non rappresenta dati multivalore (dipendenti dalla configurazione).</span><span class="sxs-lookup"><span data-stu-id="c8fa0-108">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="c8fa0-109">Ogni documento PrintCapabilities viene costruito per una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-109">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="c8fa0-110">Nessuna proprietà o ScoredProperty nel documento può avere un valore che dipende dalla configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-110">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="c8fa0-111">Nella versione dello schema iniziale, il provider PrintCapabilities deve elaborare l'input PrintTicket e creare un documento PrintCapabilities contenente i valori property appropriati per la configurazione specificata in PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-111">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="c8fa0-112">Non contiene informazioni sui vincoli.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-112">Does not contain constraint information.</span></span>

    <span data-ttu-id="c8fa0-113">Il documento PrintCapabilities non indica quali configurazioni sono consentite e quali non sono consentite.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-113">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="c8fa0-114">Nella versione iniziale dello schema, il provider PrintCapabilities deve archiviare le informazioni necessarie per convalidare le configurazioni, fornire un metodo che convalida l'input PrintTicket e restituire un PrintTicket corretto nel caso in cui il PrintTicket specificato violi uno o più vincoli.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-114">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="c8fa0-115">Non contiene informazioni dinamiche sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-115">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="c8fa0-116">La creazione del documento PrintCapabilities comporta un sovraccarico troppo alto per poter essere usato per contenere informazioni sullo stato in rapida evoluzione, ad esempio i livelli di input penna, la carta rimanente in ogni vassoio lo stato di inceppamento della carta.</span><span class="sxs-lookup"><span data-stu-id="c8fa0-116">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8fa0-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8fa0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8fa0-118">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c8fa0-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



