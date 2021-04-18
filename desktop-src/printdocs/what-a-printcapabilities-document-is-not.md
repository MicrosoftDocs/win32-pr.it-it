---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Cosa non è un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320984"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="1585a-104">Cosa non è un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="1585a-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="1585a-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1585a-105">This topic is not current.</span></span> <span data-ttu-id="1585a-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1585a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1585a-107">È utile elencare alcune funzionalità e informazioni che il documento PrintCapabilities non è destinato a fornire.</span><span class="sxs-lookup"><span data-stu-id="1585a-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="1585a-108">Documento PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="1585a-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="1585a-109">Non rappresenta dati multivalore (dipendenti dalla configurazione).</span><span class="sxs-lookup"><span data-stu-id="1585a-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="1585a-110">Ogni documento PrintCapabilities viene costruito per una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="1585a-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="1585a-111">Nessuna proprietà o ScoredProperty nel documento può avere un valore che dipende dalla configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="1585a-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="1585a-112">Nella versione iniziale dello schema, il provider PrintCapabilities deve elaborare l'oggetto PrintTicket di input e creare un documento PrintCapabilities che contiene i valori delle proprietà appropriati per la configurazione specificata nell'oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1585a-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="1585a-113">Non contiene informazioni sui vincoli.</span><span class="sxs-lookup"><span data-stu-id="1585a-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="1585a-114">Il documento PrintCapabilities non indica quali configurazioni sono consentite e quali non sono consentite.</span><span class="sxs-lookup"><span data-stu-id="1585a-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="1585a-115">Nella versione iniziale dello schema, il provider PrintCapabilities deve archiviare tutte le informazioni necessarie per convalidare le configurazioni, fornire un metodo che convalida l'oggetto PrintTicket di input e restituire un oggetto PrintTicket corretto nel caso in cui l'oggetto PrintTicket specificato violi uno o più vincoli.</span><span class="sxs-lookup"><span data-stu-id="1585a-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="1585a-116">Non contiene informazioni dinamiche sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1585a-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="1585a-117">Si è verificato un sovraccarico eccessivo nella costruzione del documento PrintCapabilities affinché venga utilizzato per mantenere le informazioni sullo stato in rapida evoluzione, ad esempio i livelli di input penna, la carta rimanente in ogni barra o lo stato di inceppamento della carta.</span><span class="sxs-lookup"><span data-stu-id="1585a-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1585a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1585a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1585a-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1585a-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



