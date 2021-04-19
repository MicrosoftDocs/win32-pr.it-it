---
description: In questa sezione viene descritto come pianificare, sviluppare e testare le pagine di riferimento per gli eventi (ERPs) e come distribuirle in un esperto o un monitoraggio. Per informazioni su ERPs e su come usarle con Network Monitor, vedere la pagina di riferimento dell'evento.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Creazione di pagine di riferimento per gli eventi Expert e monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311626"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="bbfff-104">Creazione di pagine di riferimento per gli eventi Expert e monitor</span><span class="sxs-lookup"><span data-stu-id="bbfff-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="bbfff-105">In questa sezione viene descritto come pianificare, sviluppare e testare le pagine di riferimento per gli eventi (ERPs) e come distribuirle in un esperto o un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="bbfff-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="bbfff-106">Per informazioni su ERPs e su come usarle con Network Monitor, vedere la [pagina di riferimento dell'evento](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="bbfff-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="bbfff-107">Per sviluppare un nuovo ERP, il primo passaggio consiste nel determinare gli eventi che richiedono singoli ERPs per il [monitoraggio](monitors.md)o l' [esperto](experts.md) personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bbfff-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="bbfff-108">È necessario creare ERPs separate per ogni evento che si desidera visualizzare nel Visualizzatore eventi di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="bbfff-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="bbfff-109">Si supponga, ad esempio, che:</span><span class="sxs-lookup"><span data-stu-id="bbfff-109">For example, suppose that:</span></span>

-   <span data-ttu-id="bbfff-110">Si sviluppa un monitoraggio denominato Game Monitor e stock Watcher.</span><span class="sxs-lookup"><span data-stu-id="bbfff-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="bbfff-111">Il monitoraggio si trova in un file denominato Gamemon.dll.</span><span class="sxs-lookup"><span data-stu-id="bbfff-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="bbfff-112">Il monitoraggio genera due eventi, i giochi in esecuzione e le scorte Internet aumentano.</span><span class="sxs-lookup"><span data-stu-id="bbfff-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="bbfff-113">Si prevede di sviluppare due ERPs, Gamemon1.htm e Gamemon2.htm.</span><span class="sxs-lookup"><span data-stu-id="bbfff-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="bbfff-114">Non è necessario avere una corrispondenza uno-a-uno tra ERPs per il monitoraggio o gli eventi esperti.</span><span class="sxs-lookup"><span data-stu-id="bbfff-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="bbfff-115">Dopo aver stabilito un elenco di ERPs univoche, seguire questa procedura per creare ogni ERP.</span><span class="sxs-lookup"><span data-stu-id="bbfff-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="bbfff-116">[Scrivere il documento di origine HTML](writing-an-event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="bbfff-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="bbfff-117">[Salvare e denominare](naming-an-event-reference-page.md) il file di origine HTML come file con estensione htm.</span><span class="sxs-lookup"><span data-stu-id="bbfff-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="bbfff-118">[Testare il ERP](testing-an-event-reference-page.md) con l'esperto o il monitoraggio completato.</span><span class="sxs-lookup"><span data-stu-id="bbfff-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



