---
description: Il Visualizzatore frame Network Monitor Visualizza i dati analizzati in tre riquadri.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Visualizzazione di informazioni analizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568284"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="fa052-103">Visualizzazione di informazioni analizzate</span><span class="sxs-lookup"><span data-stu-id="fa052-103">Viewing Parsed Information</span></span>

<span data-ttu-id="fa052-104">Il Visualizzatore frame Network Monitor Visualizza i dati analizzati in tre riquadri.</span><span class="sxs-lookup"><span data-stu-id="fa052-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="fa052-105">Il riquadro superiore Visualizza un riepilogo del frame che include il protocollo identificato.</span><span class="sxs-lookup"><span data-stu-id="fa052-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="fa052-106">Nel riquadro centrale vengono visualizzate le proprietà dei dati formattate che possono essere organizzate in modo gerarchico come parte della visualizzazione del parser.</span><span class="sxs-lookup"><span data-stu-id="fa052-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="fa052-107">Nel riquadro inferiore vengono visualizzati i dati non elaborati evidenziati selezionati nel riquadro centrale.</span><span class="sxs-lookup"><span data-stu-id="fa052-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="fa052-108">È possibile specificare la modalità di visualizzazione delle informazioni nel visualizzatore quando si sviluppa un parser personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fa052-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="fa052-109">Nella figura seguente viene illustrato il modo in cui le informazioni possono essere visualizzate in Network Monitor Frame Viewer.</span><span class="sxs-lookup"><span data-stu-id="fa052-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![Visualizzatore frame di Network Monitor](images/parseui.png)

> [!Note]  
> <span data-ttu-id="fa052-111">I parser non visualizzano i frame.</span><span class="sxs-lookup"><span data-stu-id="fa052-111">Parsers do not display frames.</span></span> <span data-ttu-id="fa052-112">I parser riconoscono i campi delle informazioni fornite, quindi notificano Network Monitor per visualizzare il frame.</span><span class="sxs-lookup"><span data-stu-id="fa052-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="fa052-113">Il filtro è un'operazione di livello superiore che consente di filtrare le query per estendere i parser.</span><span class="sxs-lookup"><span data-stu-id="fa052-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="fa052-114">Nel parser usare solo le funzioni che possono essere eseguite in applicazioni Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="fa052-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="fa052-115">Prima di associare le proprietà ai dati non elaborati, un parser deve prima registrare tutte le possibili proprietà con il kernel Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="fa052-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="fa052-116">Il parser Invia un messaggio al kernel per creare un database di proprietà e quindi compila il database delle proprietà con tutte le possibili proprietà del protocollo.</span><span class="sxs-lookup"><span data-stu-id="fa052-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="fa052-117">Ogni proprietà nel database delle proprietà contiene informazioni quali una descrizione testuale, un tipo di dati e un qualificatore utilizzati per formattare i dati non elaborati e una routine di formattazione utilizzata per visualizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="fa052-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 



