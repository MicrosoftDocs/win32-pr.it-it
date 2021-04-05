---
description: Una pagina di riferimento a un evento è un documento HTML che fornisce Network Monitor informazioni sugli eventi rilevati durante l'esecuzione dell'esperto o del monitoraggio.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Informazioni sulle pagine di riferimento evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882113"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="c086e-103">Informazioni sulle pagine di riferimento evento</span><span class="sxs-lookup"><span data-stu-id="c086e-103">About Event Reference Pages</span></span>

<span data-ttu-id="c086e-104">Una pagina di riferimento a un evento è un documento HTML che fornisce Network Monitor informazioni sugli eventi rilevati durante l'esecuzione dell'esperto o del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="c086e-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="c086e-105">È possibile visualizzare ERPs nel Visualizzatore eventi di Network Monitor, strumento di controllo di monitoraggio o in qualsiasi browser che supporti le funzionalità HTML di Microsoft Internet Explorer versione 4,01 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c086e-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="c086e-106">In altre lingue, è possibile aggiungere i controlli supportati o le lingue con script nell'ERP.</span><span class="sxs-lookup"><span data-stu-id="c086e-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="c086e-107">Tuttavia, ERPs vengono visualizzati solo se l'esperto designa il documento HTML in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c086e-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="c086e-108">Quando viene designato correttamente, il ERP viene visualizzato nel riquadro inferiore quando viene selezionato l'evento nel Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="c086e-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="c086e-109">La figura seguente illustra un ERP associato al monitoraggio intervallo IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="c086e-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![un ERP associato al monitoraggio intervallo IP](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="c086e-111">Eventi esperti</span><span class="sxs-lookup"><span data-stu-id="c086e-111">Expert Events</span></span>

<span data-ttu-id="c086e-112">Gli eventi esperti sono identificati dal membro **EventIdent** di una struttura [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c086e-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="c086e-113">Quando si scrive un esperto, è necessario determinare i valori **EventIdent** , che in genere sono numerati 1, 2, 3 e così via.</span><span class="sxs-lookup"><span data-stu-id="c086e-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="c086e-114">Si supponga, ad esempio, che un esperto generi due eventi (**EventIdent1** e **EventIdent2**).</span><span class="sxs-lookup"><span data-stu-id="c086e-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="c086e-115">Se si vuole che il Visualizzatore eventi visualizzi gli eventi separatamente, è necessario creare due documenti ERP distinti.</span><span class="sxs-lookup"><span data-stu-id="c086e-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 



