---
description: Il passaggio finale della creazione di una pagina di riferimento a un evento consiste nel testarlo.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Test di una pagina di riferimento a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307820"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="306b0-103">Test di una pagina di riferimento a un evento</span><span class="sxs-lookup"><span data-stu-id="306b0-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="306b0-104">Il passaggio finale della creazione di una pagina di riferimento a un evento consiste nel testarlo.</span><span class="sxs-lookup"><span data-stu-id="306b0-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="306b0-105">È possibile testare un ERP visualizzando il file in un browser HTML, ad esempio Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="306b0-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="306b0-106">In alternativa, è possibile installare il ERP e la relativa DLL di esperti per testarla per la chiamata di un evento e visualizzarla nel Visualizzatore eventi Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="306b0-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="306b0-107">Visualizzazione di ERPs senza DLL</span><span class="sxs-lookup"><span data-stu-id="306b0-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="306b0-108">Per visualizzare il ERP completato senza una DLL di esperti installata, aprire il file con un visualizzatore HTML che supporta le origini incorporate.</span><span class="sxs-lookup"><span data-stu-id="306b0-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="306b0-109">Nella figura seguente viene illustrato il file ERP di esempio descritto in [scrittura di un ERP](writing-an-event-reference-page.md) così come viene visualizzato con Microsoft Internet Explorer versione 4,01.</span><span class="sxs-lookup"><span data-stu-id="306b0-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![file ERP di esempio](images/ie-erp.png)

<span data-ttu-id="306b0-111">Test di ERPs con una DLL</span><span class="sxs-lookup"><span data-stu-id="306b0-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="306b0-112">Dopo aver creato i file ERP e la dll di [**esperti**](experts.md) , è possibile testare la funzionalità completa del ERPs con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="306b0-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="306b0-113">Si presuppone che la DLL sia sottoposta a debug e che sia in grado di generare eventi validi.</span><span class="sxs-lookup"><span data-stu-id="306b0-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="306b0-114">**Per testare ERPs che contengono una DLL**</span><span class="sxs-lookup"><span data-stu-id="306b0-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="306b0-115">Verificare che nella directory appropriata sia installata la DLL Expert corretta.</span><span class="sxs-lookup"><span data-stu-id="306b0-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="306b0-116">Per ulteriori informazioni, vedere [installazione di un esperto in Network Monitor 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="306b0-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="306b0-117">Verificare il [nome corretto](naming-an-event-reference-page.md) del file ERP.</span><span class="sxs-lookup"><span data-stu-id="306b0-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="306b0-118">Verificare il [percorso corretto](installing-existing-erps-to-network-monitor-2-1.md) di Erps nella directory Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="306b0-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="306b0-119">ERPs esperto test nell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="306b0-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="306b0-120">Genera un evento di test.</span><span class="sxs-lookup"><span data-stu-id="306b0-120">Generate a test event.</span></span>
6.  <span data-ttu-id="306b0-121">Verificare che il ERP venga visualizzato nell'Visualizzatore eventi Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="306b0-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="306b0-122">Per ulteriori informazioni sulla creazione di un ERP, vedere:</span><span class="sxs-lookup"><span data-stu-id="306b0-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="306b0-123">Creazione di pagine di riferimento per gli eventi Expert e monitor</span><span class="sxs-lookup"><span data-stu-id="306b0-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="306b0-124">Scrittura di una pagina di riferimento a un evento</span><span class="sxs-lookup"><span data-stu-id="306b0-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="306b0-125">Denominazione di una pagina di riferimento a un evento</span><span class="sxs-lookup"><span data-stu-id="306b0-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



