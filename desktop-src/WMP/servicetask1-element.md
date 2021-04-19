---
title: Elemento ServiceTask1
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento ServiceTask1 rappresenta il primo riquadro attività negozio online.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- Finestra elementi ServiceTask1 Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ca83f5f7935e8d1dfd376f569bd61f68d7e93bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328110"
---
# <a name="servicetask1-element"></a><span data-ttu-id="7a792-106">Elemento ServiceTask1</span><span class="sxs-lookup"><span data-stu-id="7a792-106">ServiceTask1 Element</span></span>

> [!Note]  
> <span data-ttu-id="7a792-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="7a792-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7a792-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7a792-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7a792-109">L'elemento **ServiceTask1** rappresenta il primo riquadro attività negozio online.</span><span class="sxs-lookup"><span data-stu-id="7a792-109">The **ServiceTask1** element represents the first online store task pane.</span></span>

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="7a792-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="7a792-110">Attributes</span></span>



| <span data-ttu-id="7a792-111">Termine</span><span class="sxs-lookup"><span data-stu-id="7a792-111">Term</span></span>                                                                                                                             | <span data-ttu-id="7a792-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a792-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7a792-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="7a792-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="7a792-114">URL per la pagina Web visualizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7a792-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="7a792-115">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="7a792-115">Parent/Child Elements</span></span>



| <span data-ttu-id="7a792-116">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="7a792-116">Hierarchy</span></span>       | <span data-ttu-id="7a792-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="7a792-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="7a792-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="7a792-118">Parent elements</span></span> | <span data-ttu-id="7a792-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="7a792-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="7a792-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7a792-120">Child elements</span></span>  | <span data-ttu-id="7a792-121">**ButtonText**, **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="7a792-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7a792-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a792-122">Remarks</span></span>

<span data-ttu-id="7a792-123">**ServiceTask1** viene considerato il riquadro attività principale per coinvolgere le attività commerciali.</span><span class="sxs-lookup"><span data-stu-id="7a792-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="7a792-124">Si tratta del riquadro attività visualizzato quando l'utente sceglie di acquistare musica.</span><span class="sxs-lookup"><span data-stu-id="7a792-124">It is the task pane that displays when the user chooses to purchase music.</span></span>

> [!Note]  
> <span data-ttu-id="7a792-125">Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="7a792-125">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="7a792-126">Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività.</span><span class="sxs-lookup"><span data-stu-id="7a792-126">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="7a792-127">Windows Media Player 11 dispone di un solo riquadro attività, rappresentato da **ServiceTask1**, che l'utente può visualizzare facendo clic sulla scheda **online stores** .</span><span class="sxs-lookup"><span data-stu-id="7a792-127">Windows Media Player 11 has only one task pane, represented by **ServiceTask1**, which the user can view by clicking on the **Online Stores** tab.</span></span>

 

<span data-ttu-id="7a792-128">I riquadri attività archivio online condividono una singola istanza del browser.</span><span class="sxs-lookup"><span data-stu-id="7a792-128">Online store task panes share a single browser instance.</span></span> <span data-ttu-id="7a792-129">Ciò significa che non è necessario scrivere codice di script nella pagina Web che si prevede di continuare a eseguire quando l'utente passa dall'attività del servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="7a792-129">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="7a792-130">Quando l'utente passa i riquadri attività, Windows Media Player archivia i cookie di sessione e l'URL.</span><span class="sxs-lookup"><span data-stu-id="7a792-130">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="7a792-131">Quando l'utente torna al riquadro attività, il lettore ripristina l'URL e i cookie.</span><span class="sxs-lookup"><span data-stu-id="7a792-131">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="7a792-132">Se l'utente sceglie di usare un archivio online diverso, i dati dell'URL e della sessione vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="7a792-132">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="7a792-133">La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.</span><span class="sxs-lookup"><span data-stu-id="7a792-133">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="7a792-134">Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="7a792-134">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="7a792-135">Nome</span><span class="sxs-lookup"><span data-stu-id="7a792-135">Name</span></span>         | <span data-ttu-id="7a792-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7a792-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a792-137">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="7a792-137">*geoid*</span></span>      | <span data-ttu-id="7a792-138">ID della posizione geografica di Windows.</span><span class="sxs-lookup"><span data-stu-id="7a792-138">Windows geographical location ID.</span></span> <span data-ttu-id="7a792-139">L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="7a792-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="7a792-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="7a792-140">*locale*</span></span>     | <span data-ttu-id="7a792-141">Windows Media Player ID impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="7a792-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="7a792-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="7a792-142">*userlocale*</span></span> | <span data-ttu-id="7a792-143">ID delle impostazioni locali di Windows.</span><span class="sxs-lookup"><span data-stu-id="7a792-143">Windows locale ID.</span></span> <span data-ttu-id="7a792-144">Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="7a792-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="7a792-145">*version*</span><span class="sxs-lookup"><span data-stu-id="7a792-145">*version*</span></span>    | <span data-ttu-id="7a792-146">Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="7a792-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="7a792-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a792-147">Requirements</span></span>



| <span data-ttu-id="7a792-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a792-148">Requirement</span></span> | <span data-ttu-id="7a792-149">Valore</span><span class="sxs-lookup"><span data-stu-id="7a792-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="7a792-150">Versione</span><span class="sxs-lookup"><span data-stu-id="7a792-150">Version</span></span><br/> | <span data-ttu-id="7a792-151">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7a792-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a792-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a792-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a792-153">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="7a792-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="7a792-154">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="7a792-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="7a792-155">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="7a792-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





