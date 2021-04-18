---
description: L'estensione dello snap-in deve visualizzare agli utenti la configurazione e le informazioni di analisi correnti.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Visualizzazione delle informazioni di configurazione e analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315353"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="fc744-103">Visualizzazione delle informazioni di configurazione e analisi</span><span class="sxs-lookup"><span data-stu-id="fc744-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="fc744-104">L'estensione dello snap-in deve visualizzare agli utenti la configurazione e le informazioni di analisi correnti.</span><span class="sxs-lookup"><span data-stu-id="fc744-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="fc744-105">Per visualizzare le informazioni, è necessario che il nodo dell'estensione dello snap-in allegati estenda gli snap-in Configurazione sicurezza utilizzando il nodo servizi.</span><span class="sxs-lookup"><span data-stu-id="fc744-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="fc744-106">Il nodo servizi è lo snap-in MMC che amministra i servizi installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fc744-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="fc744-107">I tipi di nodo che possono essere estesi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc744-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="fc744-108">Servizi di configurazione NodeType = {24a7f717-1f0c-11D1-affb-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="fc744-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="fc744-109">Inspection Services NodeType = {678050c7-1ff8-11D1-affb-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="fc744-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="fc744-110">Quando il nodo servizi è espanso, MMC notifica tutte le estensioni dello snap-in registrate.</span><span class="sxs-lookup"><span data-stu-id="fc744-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="fc744-111">Ogni snap-in allegati deve essere inserito nel nodo servizi ed eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc744-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="fc744-112">Chiamare **QueryInterface** per ottenere un puntatore all'interfaccia [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) esposta dagli snap-in configurazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fc744-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="fc744-113">Chiamare [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) per informare gli snap-in di configurazione della sicurezza che l'estensione dello snap-in è stata caricata e per stabilire un contesto per le comunicazioni.</span><span class="sxs-lookup"><span data-stu-id="fc744-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="fc744-114">Chiamare [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) per recuperare le informazioni di configurazione dal database.</span><span class="sxs-lookup"><span data-stu-id="fc744-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="fc744-115">Questo passaggio può essere eseguito quando l'estensione dello snap-in si Inizializza o quando l'utente apre il nodo.</span><span class="sxs-lookup"><span data-stu-id="fc744-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="fc744-116">Per ulteriori informazioni, vedere [aggiunta di un nodo di estensione dello snap-in allegato](adding-an-attachment-snap-in-extension-node.md).</span><span class="sxs-lookup"><span data-stu-id="fc744-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



