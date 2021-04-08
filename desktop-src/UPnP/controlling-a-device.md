---
title: Controllo di un dispositivo
description: Dopo aver individuato i dispositivi, è possibile controllarli.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856785"
---
# <a name="controlling-a-device"></a><span data-ttu-id="09872-103">Controllo di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="09872-103">Controlling a Device</span></span>

<span data-ttu-id="09872-104">Dopo aver individuato i dispositivi, è possibile controllarli.</span><span class="sxs-lookup"><span data-stu-id="09872-104">Once you have discovered devices, you can control them.</span></span>

<span data-ttu-id="09872-105">**Per visualizzare le proprietà del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="09872-105">**To view device properties**</span></span>

1.  <span data-ttu-id="09872-106">Selezionare un dispositivo nell'elenco **dispositivi trovati** .</span><span class="sxs-lookup"><span data-stu-id="09872-106">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="09872-107">Fare clic su **Proprietà dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="09872-107">Click **Device Properties**.</span></span> <span data-ttu-id="09872-108">Viene visualizzata la finestra **Proprietà dispositivo** con le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="09872-108">The **Device Properties** window appears with the requested information.</span></span>

> [!Note]  
> <span data-ttu-id="09872-109">La funzionalità di **presentazione della vista** non è disponibile nel codice di esempio C++.</span><span class="sxs-lookup"><span data-stu-id="09872-109">The **View Presentation** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="09872-110">**Per visualizzare la pagina di presentazione di un dispositivo**</span><span class="sxs-lookup"><span data-stu-id="09872-110">**To view a device's presentation page**</span></span>

1.  <span data-ttu-id="09872-111">Selezionare un dispositivo nell'elenco **dispositivi trovati** .</span><span class="sxs-lookup"><span data-stu-id="09872-111">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="09872-112">Fare clic su **Visualizza presentazione**.</span><span class="sxs-lookup"><span data-stu-id="09872-112">Click **View Presentation**.</span></span> <span data-ttu-id="09872-113">Verrà visualizzata una finestra di Internet Explorer con la pagina di presentazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="09872-113">An Internet Explorer window appears with the requested presentation page.</span></span>

> [!Note]  
> <span data-ttu-id="09872-114">Il **servizio di visualizzazione desc.** funzionalità non è disponibile nel codice di esempio C++.</span><span class="sxs-lookup"><span data-stu-id="09872-114">The **View Service Desc.** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="09872-115">**Per visualizzare la descrizione di un servizio**</span><span class="sxs-lookup"><span data-stu-id="09872-115">**To view a service description**</span></span>

1.  <span data-ttu-id="09872-116">È possibile immettere l'URL della descrizione del servizio nel **servizio desc. Campo URL** .</span><span class="sxs-lookup"><span data-stu-id="09872-116">You can enter the URL to the service description in the **Service Desc. URL** field.</span></span>

    ![URL Descrizione servizio](images/ucp-url.png)

2.  <span data-ttu-id="09872-118">Fare clic su **View Service desc.** Viene visualizzata la finestra **Visualizzatore Descrizione servizio** .</span><span class="sxs-lookup"><span data-stu-id="09872-118">Click **View Service Desc.** The **Service Description Viewer** window is displayed.</span></span> <span data-ttu-id="09872-119">È quindi possibile esplorare la descrizione del servizio utilizzando la visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="09872-119">You can then browse the service description using the tree view.</span></span> <span data-ttu-id="09872-120">Questa funzionalità non è disponibile nel codice di esempio C++.</span><span class="sxs-lookup"><span data-stu-id="09872-120">This functionality is not available in the C++ sample code.</span></span>

    ![finestra Visualizzatore Descrizione servizio](images/ucp-serv.png)

    <span data-ttu-id="09872-122">Nella finestra Visualizzatore Descrizione servizio è possibile utilizzare cinque comandi.</span><span class="sxs-lookup"><span data-stu-id="09872-122">There are five commands you can use in the Service Description Viewer window.</span></span>



| <span data-ttu-id="09872-123">Pulsante</span><span class="sxs-lookup"><span data-stu-id="09872-123">Button</span></span>                 | <span data-ttu-id="09872-124">Azione eseguita</span><span class="sxs-lookup"><span data-stu-id="09872-124">Action Performed</span></span>                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09872-125">Go</span><span class="sxs-lookup"><span data-stu-id="09872-125">Go</span></span>                     | <span data-ttu-id="09872-126">Carica il file visualizzato nella **Descrizione del servizio. Campo URL** .</span><span class="sxs-lookup"><span data-stu-id="09872-126">Loads the file shown in the **Service Desc. URL** field.</span></span>                                                                                                                              |
| <span data-ttu-id="09872-127">Imposta azione</span><span class="sxs-lookup"><span data-stu-id="09872-127">Set Action</span></span>             | <span data-ttu-id="09872-128">Selezionare un nome di azione nell'albero Descrizione servizio e fare clic su **imposta azione**.</span><span class="sxs-lookup"><span data-stu-id="09872-128">Select an action name in the service description tree and click **Set Action**.</span></span> <span data-ttu-id="09872-129">Il nome dell'azione viene immesso nel campo **azione Invoke** della finestra principale del punto di controllo dell' **utilità generico** .</span><span class="sxs-lookup"><span data-stu-id="09872-129">The action name is entered into the **Invoke Action** field of the main **Generic UCP** window.</span></span>       |
| <span data-ttu-id="09872-130">Impostare una variabile</span><span class="sxs-lookup"><span data-stu-id="09872-130">Set Variable</span></span>           | <span data-ttu-id="09872-131">Selezionare un nome di variabile nell'albero Descrizione servizio e fare clic su **Imposta variabile**.</span><span class="sxs-lookup"><span data-stu-id="09872-131">Select a variable name in the service description tree and click **Set Variable**.</span></span> <span data-ttu-id="09872-132">Il nome della variabile viene immesso nel campo **variabile query** della finestra principale del punto di controllo dell' **utilità generico** .</span><span class="sxs-lookup"><span data-stu-id="09872-132">The variable name is entered into the **Query Variable** field of the main **Generic UCP** window.</span></span> |
| <span data-ttu-id="09872-133">Popola elenco variabili</span><span class="sxs-lookup"><span data-stu-id="09872-133">Populate Variable List</span></span> | <span data-ttu-id="09872-134">Carica tutti i nomi delle variabili del servizio nell'elenco delle **variabili di query** della finestra principale del punto di controllo dell' **utilità generica** .</span><span class="sxs-lookup"><span data-stu-id="09872-134">Loads all the service's variable names into the **Query Variable** list of the main **Generic UCP** window.</span></span>                                                                           |
| <span data-ttu-id="09872-135">Popola elenco di azioni</span><span class="sxs-lookup"><span data-stu-id="09872-135">Populate Action List</span></span>   | <span data-ttu-id="09872-136">Carica tutti i nomi di azione del servizio nell'elenco di **azioni Invoke** della finestra principale del punto di controllo dell' **utilità** .</span><span class="sxs-lookup"><span data-stu-id="09872-136">Loads all the service's action names into the **Invoke Action** list of the main **Generic UCP** window.</span></span>                                                                              |



 

<span data-ttu-id="09872-137">**Per controllare un dispositivo**</span><span class="sxs-lookup"><span data-stu-id="09872-137">**To control a device**</span></span>

1.  <span data-ttu-id="09872-138">Dall'elenco **dispositivi trovati** selezionare il dispositivo che si desidera controllare.</span><span class="sxs-lookup"><span data-stu-id="09872-138">From the **Devices Found** list, select the device you want to control.</span></span>
2.  <span data-ttu-id="09872-139">Dall'elenco **Scegli servizio** selezionare il servizio da richiamare o la variabile di stato su cui si vuole eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="09872-139">From the **Choose Service** list, select the service you want to invoke or state variable you want to query.</span></span>

    ![finestra dispositivi di controllo](images/ucp-contr.png)

    > [!Note]  
    > <span data-ttu-id="09872-141">Il contenuto dell' **elenco dei servizi** è basato sul dispositivo selezionato nell'elenco **dispositivi trovati** .</span><span class="sxs-lookup"><span data-stu-id="09872-141">The contents of the **Service List** is based on the device selected in the **Devices Found** list.</span></span>

     

3.  <span data-ttu-id="09872-142">Se si desidera individuare il valore di una variabile di stato per il servizio selezionato, immettere il nome della variabile nel campo **variabile query** per servizio.</span><span class="sxs-lookup"><span data-stu-id="09872-142">If you want to find out the value of a state variable for the selected service, enter the variable name in the **Query Variable** field for service.</span></span> <span data-ttu-id="09872-143">Fare clic su **Query**.</span><span class="sxs-lookup"><span data-stu-id="09872-143">Click **Query**.</span></span> <span data-ttu-id="09872-144">I risultati vengono visualizzati nel campo **valore stato query/argomenti di azione** .</span><span class="sxs-lookup"><span data-stu-id="09872-144">The results are shown in the **Query State Value/Action Out Arguments** field.</span></span>
4.  <span data-ttu-id="09872-145">Se si desidera richiamare un'azione per un servizio, immettere il nome dell'azione nel campo **azione richiama** e gli eventuali argomenti nel campo **Argomenti azione** .</span><span class="sxs-lookup"><span data-stu-id="09872-145">If you want to invoke an action for a service, enter the action name in the **Invoke Action** field, and any arguments in the **Action Arguments** field.</span></span> <span data-ttu-id="09872-146">Fare clic su **richiama**.</span><span class="sxs-lookup"><span data-stu-id="09872-146">Click **Invoke**.</span></span> <span data-ttu-id="09872-147">I risultati vengono visualizzati nel campo **valore dello stato della query/argomenti di azione fuori** , se disponibile.</span><span class="sxs-lookup"><span data-stu-id="09872-147">The results are shown in the **Query State Value/Action Out Arguments** field, if any.</span></span>

    <span data-ttu-id="09872-148">Il valore restituito, se presente, è contenuto nel primo argomento out.</span><span class="sxs-lookup"><span data-stu-id="09872-148">The return value, if any, is contained in the first out argument.</span></span>

    > [!Note]  
    > <span data-ttu-id="09872-149">Se sono presenti più argomenti per un'azione, è necessario separarli con spazi.</span><span class="sxs-lookup"><span data-stu-id="09872-149">If there are multiple arguments for an action, separate them with spaces.</span></span>

     

5.  <span data-ttu-id="09872-150">Visualizzare le informazioni sugli eventi nel campo **eventi** per il servizio selezionato.</span><span class="sxs-lookup"><span data-stu-id="09872-150">View eventing information in the **Events** field for the selected service.</span></span>

 

 




