---
title: External. NavigateTaskPaneURL, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. NavigateTaskPaneURL, metodo
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Metodo NavigateTaskPaneURL Windows Media Player
- Metodo NavigateTaskPaneURL Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324562"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="1a5a9-107">External. NavigateTaskPaneURL, metodo</span><span class="sxs-lookup"><span data-stu-id="1a5a9-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="1a5a9-108">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1a5a9-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1a5a9-110">Il metodo **NavigateTaskPaneURL** apre una pagina Web nel riquadro attività specificato e sposta lo stato attivo sul riquadro specificato.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5a9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a5a9-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="1a5a9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a5a9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a5a9-113">*bstrKeyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-114">**Stringa** contenente il nome della chiave per l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="1a5a9-115">(obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="1a5a9-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="1a5a9-116">*bstrTaskPane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-117">**Stringa** contenente il nome del riquadro attività in cui viene visualizzata la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="1a5a9-118">(obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="1a5a9-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="1a5a9-119">*bstrParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-120">**Stringa** contenente i parametri della stringa di query da accodare all'URL specificato dall'elemento **Navigate** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="1a5a9-121">(facoltativo).</span><span class="sxs-lookup"><span data-stu-id="1a5a9-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a5a9-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a5a9-122">Return value</span></span>

<span data-ttu-id="1a5a9-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5a9-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a5a9-124">Remarks</span></span>

<span data-ttu-id="1a5a9-125">Se si passa a un riquadro non supportato dall'archivio online, è possibile che si verifichi la modifica dell'archivio online corrente.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="1a5a9-126">Il valore specificato per *bstrParams* è valido solo quando **NavigateTaskPaneURL** viene chiamato da pagine Web fornite dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="1a5a9-127">Nella tabella seguente sono elencati i valori validi per *bstrTaskPane* e il riquadro attività associato per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="1a5a9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1a5a9-128">Value</span></span>            | <span data-ttu-id="1a5a9-129">Riquadro attività</span><span class="sxs-lookup"><span data-stu-id="1a5a9-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="1a5a9-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-130">**ServiceTask1**</span></span> | <span data-ttu-id="1a5a9-131">Primo riquadro attività negozio online.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-131">First online store task pane.</span></span>  |
| <span data-ttu-id="1a5a9-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-132">**ServiceTask2**</span></span> | <span data-ttu-id="1a5a9-133">Secondo riquadro attività archivio online.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-133">Second online store task pane.</span></span> |
| <span data-ttu-id="1a5a9-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-134">**ServiceTask3**</span></span> | <span data-ttu-id="1a5a9-135">Terzo riquadro attività negozio online.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="1a5a9-136">Il codice della pagina Web deve specificare un valore per [External. SelectedTaskPane](external-selectedtaskpane.md) durante il caricamento per assicurarsi che il pulsante corretto del riquadro attività venga evidenziato dopo il completamento dello spostamento.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="1a5a9-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="1a5a9-137">Examples</span></span>

<span data-ttu-id="1a5a9-138">Il codice di esempio seguente mostra come **NavigateTaskPaneURL** crea l'URL della pagina Web da visualizzare per **ServiceTask1**.</span><span class="sxs-lookup"><span data-stu-id="1a5a9-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="1a5a9-139">Esempio dell'elemento **Navigate** :</span><span class="sxs-lookup"><span data-stu-id="1a5a9-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="1a5a9-140">Chiamata di esempio al metodo **NavigateTaskPaneURL** :</span><span class="sxs-lookup"><span data-stu-id="1a5a9-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="1a5a9-141">Esempio di URL risultante usato per la pagina Web visualizzata in **ServiceTask1**:</span><span class="sxs-lookup"><span data-stu-id="1a5a9-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="1a5a9-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a5a9-142">Requirements</span></span>



| <span data-ttu-id="1a5a9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a5a9-143">Requirement</span></span> | <span data-ttu-id="1a5a9-144">Valore</span><span class="sxs-lookup"><span data-stu-id="1a5a9-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5a9-145">Versione</span><span class="sxs-lookup"><span data-stu-id="1a5a9-145">Version</span></span><br/> | <span data-ttu-id="1a5a9-146">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1a5a9-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="1a5a9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1a5a9-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a5a9-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a5a9-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a5a9-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a5a9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5a9-150">**Oggetto esterno per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="1a5a9-151">**External. SelectedTaskPane**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





