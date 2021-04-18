---
title: Elemento ButtonText
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Finestra elementi ButtonText Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333855"
---
# <a name="buttontext-element"></a><span data-ttu-id="7fa75-105">Elemento ButtonText</span><span class="sxs-lookup"><span data-stu-id="7fa75-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="7fa75-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="7fa75-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7fa75-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7fa75-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7fa75-108">L'elemento **ButtonText** specifica la stringa di testo visualizzata da Windows Media Player per un pulsante del riquadro attività.</span><span class="sxs-lookup"><span data-stu-id="7fa75-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="7fa75-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="7fa75-109">Attributes</span></span>

<span data-ttu-id="7fa75-110">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="7fa75-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7fa75-111">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="7fa75-111">Parent/Child Elements</span></span>



| <span data-ttu-id="7fa75-112">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="7fa75-112">Hierarchy</span></span>       | <span data-ttu-id="7fa75-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="7fa75-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="7fa75-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="7fa75-114">Parent elements</span></span> | <span data-ttu-id="7fa75-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="7fa75-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="7fa75-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7fa75-116">Child elements</span></span>  | <span data-ttu-id="7fa75-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="7fa75-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="7fa75-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7fa75-118">Remarks</span></span>

<span data-ttu-id="7fa75-119">Questo elemento è obbligatorio per ogni istanza di **ServiceTask1**, **ServiceTask2** o **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="7fa75-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="7fa75-120">Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="7fa75-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="7fa75-121">Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività.</span><span class="sxs-lookup"><span data-stu-id="7fa75-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="7fa75-122">Windows Media Player 11 dispone di un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Store online** . Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="7fa75-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="7fa75-123">Windows Media Player possibile ritagliare il testo del pulsante per adattarlo allo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="7fa75-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="7fa75-124">Il lettore usa sempre il tipo di carattere Tahoma grassetto a 8 punti per questo testo.</span><span class="sxs-lookup"><span data-stu-id="7fa75-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="7fa75-125">Sono disponibili due righe per visualizzare il testo del pulsante, ma il lettore non esegue automaticamente il wrapping del testo dalla prima riga al secondo.</span><span class="sxs-lookup"><span data-stu-id="7fa75-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="7fa75-126">Per specificare un'interruzioni di riga nel testo del pulsante, inserire la nuova sequenza di escape di riga " \\ n" nella stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="7fa75-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="7fa75-127">La stringa di testo viene visualizzata anche nel menu **Vai** nell'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7fa75-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="7fa75-128">È necessario testare il negozio online usando un'ampia gamma di impostazioni di visualizzazione per garantire che il testo venga visualizzato come previsto.</span><span class="sxs-lookup"><span data-stu-id="7fa75-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa75-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fa75-129">Requirements</span></span>



| <span data-ttu-id="7fa75-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa75-130">Requirement</span></span> | <span data-ttu-id="7fa75-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7fa75-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="7fa75-132">Versione</span><span class="sxs-lookup"><span data-stu-id="7fa75-132">Version</span></span><br/> | <span data-ttu-id="7fa75-133">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7fa75-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7fa75-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fa75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa75-135">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="7fa75-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="7fa75-136">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="7fa75-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="7fa75-137">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="7fa75-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





