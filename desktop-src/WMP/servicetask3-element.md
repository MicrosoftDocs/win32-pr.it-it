---
title: Elemento ServiceTask3
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento ServiceTask3 rappresenta il terzo riquadro attività negozio online.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- Finestra elementi ServiceTask3 Media Player
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d78b9e70c7e6933693f4d29750e9e3c0b4e897a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333107"
---
# <a name="servicetask3-element"></a><span data-ttu-id="a4a3c-106">Elemento ServiceTask3</span><span class="sxs-lookup"><span data-stu-id="a4a3c-106">ServiceTask3 Element</span></span>

> [!Note]  
> <span data-ttu-id="a4a3c-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a4a3c-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a4a3c-109">L'elemento **ServiceTask3** rappresenta il terzo riquadro attività negozio online.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-109">The **ServiceTask3** element represents the third online store task pane.</span></span>

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="a4a3c-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="a4a3c-110">Attributes</span></span>



| <span data-ttu-id="a4a3c-111">Termine</span><span class="sxs-lookup"><span data-stu-id="a4a3c-111">Term</span></span>                                                                                                                             | <span data-ttu-id="a4a3c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4a3c-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a4a3c-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="a4a3c-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="a4a3c-114">URL per la pagina Web visualizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="a4a3c-115">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="a4a3c-115">Parent/Child Elements</span></span>



| <span data-ttu-id="a4a3c-116">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="a4a3c-116">Hierarchy</span></span>       | <span data-ttu-id="a4a3c-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="a4a3c-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="a4a3c-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a4a3c-118">Parent elements</span></span> | <span data-ttu-id="a4a3c-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a4a3c-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="a4a3c-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a4a3c-120">Child elements</span></span>  | <span data-ttu-id="a4a3c-121">**ButtonText**, **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="a4a3c-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a4a3c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4a3c-122">Remarks</span></span>

<span data-ttu-id="a4a3c-123">**ServiceTask1** viene considerato il riquadro attività principale per coinvolgere le attività commerciali.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="a4a3c-124">Si tratta del riquadro attività visualizzato quando l'utente sceglie di acquistare musica.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-124">It is the task pane that displays when the user chooses to purchase music.</span></span> <span data-ttu-id="a4a3c-125">Usare **ServiceTask3** per altre attività di archivio online.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-125">Use **ServiceTask3** for other online store activity.</span></span>

> [!Note]  
> <span data-ttu-id="a4a3c-126">Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-126">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="a4a3c-127">Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-127">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="a4a3c-128">Windows Media Player 11 dispone di un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Store online** . Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="a4a3c-128">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="a4a3c-129">I riquadri attività negozi online condividono una singola istanza del browser.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-129">Online stores task panes share a single browser instance.</span></span> <span data-ttu-id="a4a3c-130">Ciò significa che non è necessario scrivere codice di script nella pagina Web che si prevede di continuare a eseguire quando l'utente passa dall'attività del servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-130">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="a4a3c-131">Quando l'utente passa i riquadri attività, Windows Media Player archivia i cookie di sessione e l'URL.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-131">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="a4a3c-132">Quando l'utente torna al riquadro attività, il lettore ripristina l'URL e i cookie.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-132">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="a4a3c-133">Se l'utente sceglie di usare un archivio online diverso, i dati dell'URL e della sessione vengono cancellati.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-133">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="a4a3c-134">La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-134">The following table details the parameters sent with the URL request.</span></span>



| <span data-ttu-id="a4a3c-135">Nome</span><span class="sxs-lookup"><span data-stu-id="a4a3c-135">Name</span></span>         | <span data-ttu-id="a4a3c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a4a3c-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a3c-137">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="a4a3c-137">*geoid*</span></span>      | <span data-ttu-id="a4a3c-138">ID della posizione geografica di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-138">Windows geographical location ID.</span></span> <span data-ttu-id="a4a3c-139">L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="a4a3c-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="a4a3c-140">*locale*</span></span>     | <span data-ttu-id="a4a3c-141">Windows Media Player ID impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="a4a3c-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="a4a3c-142">*userlocale*</span></span> | <span data-ttu-id="a4a3c-143">ID delle impostazioni locali di Windows.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-143">Windows locale ID.</span></span> <span data-ttu-id="a4a3c-144">Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="a4a3c-145">*version*</span><span class="sxs-lookup"><span data-stu-id="a4a3c-145">*version*</span></span>    | <span data-ttu-id="a4a3c-146">Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a4a3c-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4a3c-147">Requirements</span></span>



| <span data-ttu-id="a4a3c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a3c-148">Requirement</span></span> | <span data-ttu-id="a4a3c-149">Valore</span><span class="sxs-lookup"><span data-stu-id="a4a3c-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="a4a3c-150">Versione</span><span class="sxs-lookup"><span data-stu-id="a4a3c-150">Version</span></span><br/> | <span data-ttu-id="a4a3c-151">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4a3c-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4a3c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a3c-153">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="a4a3c-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="a4a3c-154">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="a4a3c-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="a4a3c-155">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="a4a3c-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





