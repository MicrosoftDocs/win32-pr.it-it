---
title: Proprietà Command. suggerimento
description: Rappresenta il suggerimento tasto di ricerca per un controllo.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Barra multifunzione di Windows della proprietà Command. suggerimento
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302317"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="67f1a-104">Proprietà Command. suggerimento</span><span class="sxs-lookup"><span data-stu-id="67f1a-104">Command.Keytip property</span></span>

<span data-ttu-id="67f1a-105">Rappresenta il suggerimento tasto di ricerca per un controllo.</span><span class="sxs-lookup"><span data-stu-id="67f1a-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="67f1a-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="67f1a-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="67f1a-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="67f1a-107">Attributes</span></span>

<span data-ttu-id="67f1a-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="67f1a-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="67f1a-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="67f1a-109">Child elements</span></span>



| <span data-ttu-id="67f1a-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="67f1a-110">Element</span></span>                                                   | <span data-ttu-id="67f1a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67f1a-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="67f1a-112">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="67f1a-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="67f1a-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="67f1a-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="67f1a-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="67f1a-114">Parent elements</span></span>



| <span data-ttu-id="67f1a-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="67f1a-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="67f1a-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="67f1a-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="67f1a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="67f1a-117">Remarks</span></span>

<span data-ttu-id="67f1a-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67f1a-118">Optional.</span></span>

<span data-ttu-id="67f1a-119">Può verificarsi al massimo una volta per ogni elemento [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="67f1a-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="67f1a-120">**Command. suggerimento. suggerimento** può contenere un valore di tipo *xs: String* vincolato a qualsiasi sequenza di caratteri Unicode, incluso lo spazio vuoto.</span><span class="sxs-lookup"><span data-stu-id="67f1a-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="67f1a-121">Un **comando. suggerimento suggerimento** può iniziare con un numero solo se associato a un controllo all'interno di una [scheda](windowsribbon-controls-tab.md) o della [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="67f1a-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="67f1a-122">Per visualizzare i suggerimenti tasti validi per lo stato corrente della barra multifunzione, tenere premuto ALT.</span><span class="sxs-lookup"><span data-stu-id="67f1a-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="67f1a-123">Lo screenshot seguente mostra i suggerimenti di tasti iniziali, o di primo livello, visualizzati in Microsoft Paint per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67f1a-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="67f1a-124">Dopo aver selezionato un suggerimento tasto di scelta di primo livello, vengono visualizzati solo i suggerimenti tasti di secondo livello.</span><span class="sxs-lookup"><span data-stu-id="67f1a-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![suggerimenti dei tasti di primo livello in Microsoft Paint per Windows 7](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="67f1a-126">**Command.** hotkey funge da tasto di scelta rapida per un comando, a meno che il comando non venga esposto tramite una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="67f1a-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="67f1a-127">In questo caso, il Framework ignora il valore **Command. suggerimento** e usa invece un carattere preceduto da una e commerciale come specificato da [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [dall' \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="67f1a-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="67f1a-128">Se nessuna e commerciale è specificata da **Command. LabelTitle** o dall'etichetta pkey dell'interfaccia utente \_ \_ , non viene esposto alcun tasto di scelta rapida o tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="67f1a-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="67f1a-129">Se non viene specificato alcun valore per **Command. suggerimento**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="67f1a-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="67f1a-130">Se **Command. textsuggerimento** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="67f1a-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="67f1a-131">Per impostazione predefinita, le lettere seguenti vengono usate dal Framework per generare automaticamente i suggerimenti dei tasti:</span><span class="sxs-lookup"><span data-stu-id="67f1a-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="67f1a-132">**F** viene assegnato al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="67f1a-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="67f1a-133">**Y** viene assegnato a qualsiasi comando che non dispone di un tasto di suggerimento specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67f1a-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="67f1a-134">La **Z** viene assegnata a ogni controllo del [gruppo](windowsribbon-controls-group.md) e non può essere personalizzata.</span><span class="sxs-lookup"><span data-stu-id="67f1a-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="67f1a-135">Un suggerimento tasto di gruppo viene visualizzato solo quando [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) per il controllo specifica un'opzione di dimensioni **popup** .</span><span class="sxs-lookup"><span data-stu-id="67f1a-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="67f1a-136">Per ulteriori informazioni, vedere [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="67f1a-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="67f1a-137">Nessuna di queste lettere è riservata dal Framework.</span><span class="sxs-lookup"><span data-stu-id="67f1a-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="67f1a-138">Ogni può essere assegnato a uno o più comandi in modo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="67f1a-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="67f1a-139">Il Framework risolve i conflitti del tasto di suggerimento nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="67f1a-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="67f1a-140">Se uno o più controlli struttura a schede sono associati allo stesso suggerimento tasto di aggiunta, viene aggiunto un numero a ogni suggerimento [tasto](windowsribbon-controls-tab.md) di ricerca, a partire da 1 e aumentando in sequenza (2, 3,...) per ogni controllo nell'ordine di dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="67f1a-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="67f1a-141">Se ai controlli a schede viene assegnata la lettera F come suggerimento tasto di scelta, al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) viene assegnato F1 con i suggerimenti di tasti rimanenti, come descritto.</span><span class="sxs-lookup"><span data-stu-id="67f1a-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="67f1a-142">Quando è associato a un singolo controllo all'interno di una [scheda](windowsribbon-controls-tab.md), il suggerimento tasto F è valido sia per il controllo che per il [menu applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="67f1a-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="67f1a-143">Il tasto di scelta rapida del menu applicazione predefinito non viene modificato, ma la precedenza viene assegnata al controllo nella scheda attiva.</span><span class="sxs-lookup"><span data-stu-id="67f1a-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="67f1a-144">Se uno o più controlli all'interno di una scheda sono associati allo stesso [tasto](windowsribbon-controls-tab.md) di suggerimento, il Framework esegue automaticamente il refactoring dei suggerimenti di questi controlli, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="67f1a-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="67f1a-145">Una lieve variazione del colore del testo viene usata per evidenziare i suggerimenti per i tasti di refactoring in un'implementazione standard della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="67f1a-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="67f1a-146">Per un'implementazione della barra multifunzione non standard in cui il colore della barra multifunzione è stato personalizzato, viene eseguito l'override di questo comportamento del Framework e vengono visualizzati tutti i suggerimenti dei tasti con lo stesso colore del testo.</span><span class="sxs-lookup"><span data-stu-id="67f1a-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="67f1a-147">Per ulteriori informazioni, vedere [personalizzazione dei colori della barra multifunzione](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="67f1a-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="67f1a-148">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="67f1a-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="67f1a-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="67f1a-149">Examples</span></span>

<span data-ttu-id="67f1a-150">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. suggerimento** .</span><span class="sxs-lookup"><span data-stu-id="67f1a-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="67f1a-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67f1a-151">Requirements</span></span>



| <span data-ttu-id="67f1a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f1a-152">Requirement</span></span> | <span data-ttu-id="67f1a-153">Valore</span><span class="sxs-lookup"><span data-stu-id="67f1a-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="67f1a-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67f1a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="67f1a-155">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="67f1a-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="67f1a-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67f1a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="67f1a-157">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="67f1a-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67f1a-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67f1a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f1a-159">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="67f1a-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





