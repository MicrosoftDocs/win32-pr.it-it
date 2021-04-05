---
title: Recupero delle informazioni sullo stato
description: Recupero delle informazioni sullo stato
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, recupero dello stato
- archivi online, recupero dello stato
- digitare 2 archivi online, recupero dello stato
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- recupero dello stato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712721"
---
# <a name="retrieving-status-information"></a><span data-ttu-id="83dac-113">Recupero delle informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="83dac-113">Retrieving Status Information</span></span>

<span data-ttu-id="83dac-114">Le informazioni sullo stato vengono aggiornate utilizzando il timer creato nella funzione **init** .</span><span class="sxs-lookup"><span data-stu-id="83dac-114">Status information is updated using the timer created in the **Init** function.</span></span> <span data-ttu-id="83dac-115">Tutti gli Stati vengono aggiornati utilizzando lo stesso timer.</span><span class="sxs-lookup"><span data-stu-id="83dac-115">All status is updated using the same timer.</span></span> <span data-ttu-id="83dac-116">Il nome della funzione per l'evento timer è **OnTimer**.</span><span class="sxs-lookup"><span data-stu-id="83dac-116">The name of the function for the timer event is **OnTimer**.</span></span>

<span data-ttu-id="83dac-117">**OnTimer** determina le informazioni da visualizzare in base alla selezione dell'utente, archiviata nella variabile globale denominata g \_ oCurrentDLItem.</span><span class="sxs-lookup"><span data-stu-id="83dac-117">**OnTimer** determines the information to display based upon the user selection, which is stored in the global variable named g\_oCurrentDLItem.</span></span> <span data-ttu-id="83dac-118">La funzione verifica prima di tutto se i valori di dimensioni o di avanzamento sono validi e crea una stringa per ogni case.</span><span class="sxs-lookup"><span data-stu-id="83dac-118">The function first tests whether the size or progress values are valid and creates a string for each case.</span></span>


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



<span data-ttu-id="83dac-119">Se un valore è valido, la stringa rappresenta il numero di byte.</span><span class="sxs-lookup"><span data-stu-id="83dac-119">If a value is valid, the string represents the byte count.</span></span> <span data-ttu-id="83dac-120">Se il valore non è valido, ad esempio-1, la stringa fornisce un messaggio per informare l'utente che le informazioni non sono ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="83dac-120">If the value is not valid, such as -1, the string provides a message to inform the user that the information is not yet available.</span></span>

<span data-ttu-id="83dac-121">Successivamente, un blocco **Switch** determina se il download per l'elemento selezionato è stato completato o annullato.</span><span class="sxs-lookup"><span data-stu-id="83dac-121">Next, a **switch** block determines whether the download for the selected item is completed or canceled.</span></span> <span data-ttu-id="83dac-122">Se uno dei due casi è true, il valore della dimensione delle variabili o dello stato di avanzamento viene aggiornato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="83dac-122">If either case is true, the value of the variables Size or Progress is updated accordingly.</span></span>


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



<span data-ttu-id="83dac-123">Infine, le informazioni sullo stato vengono visualizzate nell'elemento DIV denominato dlstate.</span><span class="sxs-lookup"><span data-stu-id="83dac-123">Finally, the status information is displayed in the DIV element named dlstate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83dac-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83dac-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83dac-125">**Uso di Download Manager**</span><span class="sxs-lookup"><span data-stu-id="83dac-125">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




