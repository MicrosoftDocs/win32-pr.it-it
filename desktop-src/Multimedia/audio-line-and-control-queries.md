---
title: Query di controllo e linea audio
description: Query di controllo e linea audio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimediale, controlli Mixer
- audio, controlli Mixer
- mixer audio, linee audio
- linee audio
- mixer audio, controlli
- mixer, controlli
- mixer, linee audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725087"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="e9067-110">Query di controllo e linea audio</span><span class="sxs-lookup"><span data-stu-id="e9067-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="e9067-111">I servizi mixer forniscono funzioni per determinare le informazioni sulle linee audio, i controlli della linea audio e i dettagli del controllo.</span><span class="sxs-lookup"><span data-stu-id="e9067-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="e9067-112">I servizi forniscono anche funzioni per l'impostazione dei dettagli del controllo.</span><span class="sxs-lookup"><span data-stu-id="e9067-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="e9067-113">È possibile utilizzare la funzione [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) per recuperare informazioni su una linea audio specificata.</span><span class="sxs-lookup"><span data-stu-id="e9067-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="e9067-114">Questa funzione riempie la struttura [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) per una linea audio di origine, una linea audio di destinazione o un identificatore di riga specificati.</span><span class="sxs-lookup"><span data-stu-id="e9067-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="e9067-115">La struttura include il numero di riga di destinazione, il numero di canali nella linea audio, oltre a un nome breve e lungo per la linea audio.</span><span class="sxs-lookup"><span data-stu-id="e9067-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="e9067-116">La funzione [**mixerGetlineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera informazioni generali su uno o più controlli associati a una linea audio.</span><span class="sxs-lookup"><span data-stu-id="e9067-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="e9067-117">Questa funzione riempie la struttura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) con le informazioni sul controllo o sui controlli specificati.</span><span class="sxs-lookup"><span data-stu-id="e9067-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="e9067-118">È possibile usare **mixerGetlineControls** per recuperare le proprietà dei controlli per uno degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9067-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="e9067-119">Tutti i controlli per una riga di codice sorgente specificata</span><span class="sxs-lookup"><span data-stu-id="e9067-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="e9067-120">Controllo specificato per una riga di codice sorgente specificata</span><span class="sxs-lookup"><span data-stu-id="e9067-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="e9067-121">Primo controllo di una classe specifica per una riga di codice sorgente specificata</span><span class="sxs-lookup"><span data-stu-id="e9067-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="e9067-122">La funzione [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera le proprietà di un singolo controllo associato a una linea audio.</span><span class="sxs-lookup"><span data-stu-id="e9067-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="e9067-123">Questa funzione riempie la struttura [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) con i valori correnti per un controllo.</span><span class="sxs-lookup"><span data-stu-id="e9067-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="e9067-124">La funzione [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa il contenuto della struttura **MIXERCONTROLDETAILS** per impostare le proprietà del controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="e9067-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="e9067-125">È necessario assicurarsi che tutti i membri di questa struttura vengano riempiti prima di chiamare **mixerSetControlDetails**.</span><span class="sxs-lookup"><span data-stu-id="e9067-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 