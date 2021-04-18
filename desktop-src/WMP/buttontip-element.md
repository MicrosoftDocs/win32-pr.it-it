---
title: Elemento ButtonTip
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Finestra elementi ButtonTip Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324836"
---
# <a name="buttontip-element"></a><span data-ttu-id="b46dd-105">Elemento ButtonTip</span><span class="sxs-lookup"><span data-stu-id="b46dd-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="b46dd-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="b46dd-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b46dd-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b46dd-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b46dd-108">L'elemento **ButtonTip** specifica la stringa di testo visualizzata quando l'utente fa riferimento a un pulsante del riquadro attività.</span><span class="sxs-lookup"><span data-stu-id="b46dd-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="b46dd-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="b46dd-109">Attributes</span></span>

<span data-ttu-id="b46dd-110">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="b46dd-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b46dd-111">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="b46dd-111">Parent/Child Elements</span></span>



| <span data-ttu-id="b46dd-112">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="b46dd-112">Hierarchy</span></span>       | <span data-ttu-id="b46dd-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="b46dd-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="b46dd-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b46dd-114">Parent elements</span></span> | <span data-ttu-id="b46dd-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="b46dd-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="b46dd-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b46dd-116">Child elements</span></span>  | <span data-ttu-id="b46dd-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="b46dd-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b46dd-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b46dd-118">Remarks</span></span>

<span data-ttu-id="b46dd-119">Questo elemento è facoltativo per ogni istanza di **ServiceTask1**, **ServiceTask2** o **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="b46dd-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="b46dd-120">Se questo elemento non viene specificato, Windows Media Player usa il testo del pulsante come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b46dd-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="b46dd-121">Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="b46dd-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="b46dd-122">Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività.</span><span class="sxs-lookup"><span data-stu-id="b46dd-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="b46dd-123">Windows Media Player 11 dispone di un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Store online** . Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="b46dd-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b46dd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b46dd-124">Requirements</span></span>



| <span data-ttu-id="b46dd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b46dd-125">Requirement</span></span> | <span data-ttu-id="b46dd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b46dd-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="b46dd-127">Versione</span><span class="sxs-lookup"><span data-stu-id="b46dd-127">Version</span></span><br/> | <span data-ttu-id="b46dd-128">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b46dd-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b46dd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b46dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b46dd-130">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b46dd-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b46dd-131">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="b46dd-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b46dd-132">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b46dd-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





