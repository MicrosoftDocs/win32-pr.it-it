---
title: Proprietà Command. LabelDescription
description: Rappresenta una descrizione dell'etichetta.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Barra multifunzione di Windows Command. LabelDescription
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964769"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="bf3b8-104">Proprietà Command. LabelDescription</span><span class="sxs-lookup"><span data-stu-id="bf3b8-104">Command.LabelDescription property</span></span>

<span data-ttu-id="bf3b8-105">Rappresenta una descrizione dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="bf3b8-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bf3b8-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="bf3b8-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="bf3b8-107">Attributes</span></span>

<span data-ttu-id="bf3b8-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bf3b8-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bf3b8-109">Child elements</span></span>



| <span data-ttu-id="bf3b8-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf3b8-110">Element</span></span>                                                   | <span data-ttu-id="bf3b8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf3b8-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="bf3b8-112">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="bf3b8-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="bf3b8-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="bf3b8-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bf3b8-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="bf3b8-114">Parent elements</span></span>



| <span data-ttu-id="bf3b8-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf3b8-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="bf3b8-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="bf3b8-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bf3b8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf3b8-117">Remarks</span></span>

<span data-ttu-id="bf3b8-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-118">Optional.</span></span>

<span data-ttu-id="bf3b8-119">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="bf3b8-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="bf3b8-120">**Command. LabelDescription** può contenere un valore di *tipo xs: String* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="bf3b8-121">Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="bf3b8-122">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="bf3b8-123">Se non viene specificato alcun valore per **Command. LabelDescription**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="bf3b8-124">Se **Command. LabelDescription** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="bf3b8-125">**Command. LabelDescription** supporta solo l'allineamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="bf3b8-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="bf3b8-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf3b8-126">Examples</span></span>

<span data-ttu-id="bf3b8-127">Nell'esempio seguente viene illustrato un manifesto di comandi degli Appunti con diverse dichiarazioni **Command. LabelDescription** .</span><span class="sxs-lookup"><span data-stu-id="bf3b8-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



## <a name="requirements"></a><span data-ttu-id="bf3b8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf3b8-128">Requirements</span></span>



| <span data-ttu-id="bf3b8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf3b8-129">Requirement</span></span> | <span data-ttu-id="bf3b8-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bf3b8-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bf3b8-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf3b8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bf3b8-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf3b8-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bf3b8-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf3b8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bf3b8-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf3b8-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf3b8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf3b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf3b8-136">Interfaccia utente \_ pkey \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="bf3b8-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





