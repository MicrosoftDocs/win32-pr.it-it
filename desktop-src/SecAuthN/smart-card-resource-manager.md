---
description: Gestione risorse smart card
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gestione risorse smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316223"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="bda50-103">Gestione risorse smart card</span><span class="sxs-lookup"><span data-stu-id="bda50-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="bda50-104">Il [*gestore di risorse*](../secgloss/r-gly.md) della [*Smart Card*](../secgloss/s-gly.md) gestisce l'accesso ai [*lettori*](../secgloss/r-gly.md) e alle *Smart Card*.</span><span class="sxs-lookup"><span data-stu-id="bda50-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="bda50-105">Per gestire queste risorse, vengono eseguite le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="bda50-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="bda50-106">Identifica e tiene traccia delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bda50-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="bda50-107">Alloca Reader e risorse tra più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bda50-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="bda50-108">Supporta le primitive [*delle transazioni*](../secgloss/t-gly.md) per accedere ai servizi disponibili in una scheda specifica.</span><span class="sxs-lookup"><span data-stu-id="bda50-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="bda50-109">Si tratta di un punto importante perché le schede correnti sono dispositivi a thread singolo che richiedono spesso l'esecuzione di più comandi per completare una singola funzione.</span><span class="sxs-lookup"><span data-stu-id="bda50-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="bda50-110">[*Le transazioni*](../secgloss/t-gly.md) consentono l'esecuzione di più comandi senza interruzioni, assicurando che le informazioni [*sullo stato*](../secgloss/s-gly.md) intermedio non siano danneggiate.</span><span class="sxs-lookup"><span data-stu-id="bda50-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="bda50-111">È possibile accedere a Resource Manager direttamente tramite l'API di Resource Manager o indirettamente tramite qualsiasi [*provider di servizi*](../secgloss/s-gly.md)smart card.</span><span class="sxs-lookup"><span data-stu-id="bda50-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="bda50-112">L'API di Resource Manager è un set di funzioni di Windows che consentono l'accesso diretto ai servizi di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="bda50-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="bda50-113">Per una panoramica delle funzioni di Windows fornite dall'API, vedere [Smart Card gestione risorse API](smart-card-resource-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="bda50-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="bda50-114">In confronto, i provider di servizi Smart Card utilizzano le interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="bda50-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="bda50-115">Molte delle funzioni di Windows nell'API di Resource Manager hanno equivalenti nelle proprietà e nei metodi delle interfacce COM dei provider di servizi Smart Card.</span><span class="sxs-lookup"><span data-stu-id="bda50-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="bda50-116">Anche se la maggior parte degli sviluppatori di applicazioni troverà COM più semplice da usare, alcune applicazioni dovranno ancora usare le funzioni di Windows per eseguire determinate attività.</span><span class="sxs-lookup"><span data-stu-id="bda50-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="bda50-117">Ad esempio, le applicazioni che devono modificare l'elenco di Reader o gruppi di lettori nel [*database delle smart card*](../secgloss/s-gly.md)e quelle che richiedono il controllo diretto di un lettore devono usare l'API di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="bda50-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="bda50-118">I servizi che forniscono queste funzionalità sono disponibili solo nelle funzioni di Windows e non nel COM fornito dai provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="bda50-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="bda50-119">Per informazioni sulle modalità di implementazione di [*Resource Manager*](../secgloss/r-gly.md) in Windows, vedere [Gestione risorse implementazione](resource-manager-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="bda50-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
