---
title: Modifica della proprietà del plug-in audio DSP di esempio
description: Modifica della proprietà del plug-in audio DSP di esempio
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in DSP audio, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712184"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a><span data-ttu-id="58122-108">Modifica della proprietà del plug-in audio DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="58122-108">Changing the Sample Audio DSP Plug-in Property</span></span>

<span data-ttu-id="58122-109">È probabile che si desideri modificare la proprietà creata dalla procedura guidata plug-in di Windows Media Player per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="58122-109">You will probably want to change the property that the Windows Media Player Plug-in Wizard creates by default.</span></span> <span data-ttu-id="58122-110">Nell'elenco seguente vengono illustrati in dettaglio gli elementi che potrebbero richiedere modifiche:</span><span class="sxs-lookup"><span data-stu-id="58122-110">The following list details the items that might require changing:</span></span>

-   <span data-ttu-id="58122-111">**Risorsa della finestra di dialogo.**</span><span class="sxs-lookup"><span data-stu-id="58122-111">**The dialog resource.**</span></span> <span data-ttu-id="58122-112">Fare clic sulla scheda **ResourceView** nella finestra dell'area di lavoro progetto.</span><span class="sxs-lookup"><span data-stu-id="58122-112">Click the **ResourceView** tab in the Project Workspace window.</span></span> <span data-ttu-id="58122-113">Espandere l'elenco di cartelle per aprire la cartella della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="58122-113">Expand the folder list to open the Dialog folder.</span></span> <span data-ttu-id="58122-114">Fare doppio clic sulla risorsa finestra di dialogo per aprire l'editor risorse.</span><span class="sxs-lookup"><span data-stu-id="58122-114">Double-click the dialog resource to open the resource editor.</span></span> <span data-ttu-id="58122-115">È possibile apportare modifiche alla finestra di dialogo della pagina delle proprietà per soddisfare le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="58122-115">You can make changes to the property page dialog to fulfill your needs.</span></span> <span data-ttu-id="58122-116">Ad esempio, è possibile modificare il testo nell'etichetta o sostituire il controllo di modifica con una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="58122-116">For instance, you could change the text in the label or replace the edit control with a checkbox.</span></span>
-   <span data-ttu-id="58122-117">**Codice dell'oggetto della pagina delle proprietà.**</span><span class="sxs-lookup"><span data-stu-id="58122-117">**The property page object code.**</span></span> <span data-ttu-id="58122-118">L'implementazione predefinita usa una variabile di tipo Double per archiviare il fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="58122-118">The default implementation uses a variable of type double to store the scale factor.</span></span> <span data-ttu-id="58122-119">Potrebbe essere necessario un tipo di dati diverso.</span><span class="sxs-lookup"><span data-stu-id="58122-119">You might require a different type of data.</span></span> <span data-ttu-id="58122-120">Questa operazione richiede anche la modifica del codice che rende permanente i dati nel registro di sistema e legge i dati dal registro di sistema (incluso il codice che legge dal registro di sistema in *CProjectName*::**FinalConstruct**).</span><span class="sxs-lookup"><span data-stu-id="58122-120">This would also require you to change the code that persists the data to the registry and reads the data from the registry (including the code that reads from the registry in *CProjectName*::**FinalConstruct**).</span></span>
-   <span data-ttu-id="58122-121">**Variabile membro che archivia il valore della proprietà.**</span><span class="sxs-lookup"><span data-stu-id="58122-121">**The member variable that stores the property value.**</span></span> <span data-ttu-id="58122-122">Questa variabile è denominata "m \_ fScaleFactor" ed è dichiarata come tipo Double.</span><span class="sxs-lookup"><span data-stu-id="58122-122">This variable is named "m\_fScaleFactor" and is declared as type double.</span></span> <span data-ttu-id="58122-123">Potrebbe essere necessario modificare il nome e il tipo di questa variabile in tutto il progetto.</span><span class="sxs-lookup"><span data-stu-id="58122-123">You may want to change the name and type of this variable throughout the project.</span></span>
-   <span data-ttu-id="58122-124">**Metodi get e Property put della proprietà.**</span><span class="sxs-lookup"><span data-stu-id="58122-124">**The property get and property put methods.**</span></span> <span data-ttu-id="58122-125">Potrebbe essere necessario modificare i nomi, i parametri e le implementazioni di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="58122-125">You might want to change the names, parameters, and implementations of these methods.</span></span> <span data-ttu-id="58122-126">Non dimenticare di riflettere anche le modifiche apportate altrove nel progetto.</span><span class="sxs-lookup"><span data-stu-id="58122-126">Don't forget to also reflect those changes elsewhere in the project.</span></span> <span data-ttu-id="58122-127">Ad esempio, la pagina delle proprietà **Apply** Method chiama *CProjectName*::**put \_ scale**.</span><span class="sxs-lookup"><span data-stu-id="58122-127">For instance, the property page **Apply** method calls *CProjectName*::**put\_scale**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58122-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58122-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58122-129">**Implementazione di un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="58122-129">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




