---
title: Proprietà Command. LabelTitle
description: Rappresenta il titolo di un'etichetta.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Barra multifunzione di Windows Command. LabelTitle
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518688"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="309fe-104">Proprietà Command. LabelTitle</span><span class="sxs-lookup"><span data-stu-id="309fe-104">Command.LabelTitle property</span></span>

<span data-ttu-id="309fe-105">Rappresenta il titolo di un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="309fe-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="309fe-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="309fe-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="309fe-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="309fe-107">Attributes</span></span>

<span data-ttu-id="309fe-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="309fe-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="309fe-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="309fe-109">Child elements</span></span>



| <span data-ttu-id="309fe-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="309fe-110">Element</span></span>                                                   | <span data-ttu-id="309fe-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="309fe-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="309fe-112">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="309fe-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="309fe-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="309fe-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="309fe-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="309fe-114">Parent elements</span></span>



| <span data-ttu-id="309fe-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="309fe-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="309fe-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="309fe-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="309fe-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="309fe-117">Remarks</span></span>

<span data-ttu-id="309fe-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="309fe-118">Optional.</span></span>

<span data-ttu-id="309fe-119">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="309fe-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="309fe-120">**Command. LabelTitle** può contenere un valore di tipo *xs: String* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="309fe-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="309fe-121">Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="309fe-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="309fe-122">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="309fe-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="309fe-123">Se non viene specificato alcun valore per **Command. LabelTitle**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="309fe-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="309fe-124">Se **Command. LabelTitle** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="309fe-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="309fe-125">**Command. LabelTitle** supporta solo l'allineamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="309fe-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="309fe-126">Se un comando viene esposto tramite una voce di menu e il valore di **Command. LabelTitle** o dell' [ \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md) contiene una lettera preceduta da una e commerciale, come illustrato nell'esempio seguente, questa lettera viene considerata come un tasto di scelta rapida e un tasto di scelta rapida per tale comando dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="309fe-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="309fe-127">Per visualizzare una e commerciale in un'etichetta, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( `&&` ), come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="309fe-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="309fe-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="309fe-128">Examples</span></span>

<span data-ttu-id="309fe-129">Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. LabelTitle** .</span><span class="sxs-lookup"><span data-stu-id="309fe-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="309fe-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="309fe-130">Requirements</span></span>



| <span data-ttu-id="309fe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="309fe-131">Requirement</span></span> | <span data-ttu-id="309fe-132">Valore</span><span class="sxs-lookup"><span data-stu-id="309fe-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="309fe-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="309fe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="309fe-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="309fe-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="309fe-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="309fe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="309fe-136">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="309fe-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="309fe-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="309fe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="309fe-138">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="309fe-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





