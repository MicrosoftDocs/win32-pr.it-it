---
title: Proprietà Application. Commands
description: Rappresenta un contenitore per tutti i comandi definiti dall'applicazione.
ms.assetid: 160d7d28-2d64-4cbc-b2b9-2da6b2f5b3c8
keywords:
- Proprietà Application. Commands barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Application.Commands
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de2b88b97dda96636a9c5da3ad078f678091d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476667"
---
# <a name="applicationcommands-property"></a><span data-ttu-id="9f767-104">Proprietà Application. Commands</span><span class="sxs-lookup"><span data-stu-id="9f767-104">Application.Commands property</span></span>

<span data-ttu-id="9f767-105">Rappresenta un contenitore per tutti i comandi definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f767-105">Represents a container for all the Commands that are defined by the application.</span></span>

## <a name="usage"></a><span data-ttu-id="9f767-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9f767-106">Usage</span></span>

``` syntax
<Application.Commands>
  child elements
</Application.Commands>
```

## <a name="attributes"></a><span data-ttu-id="9f767-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="9f767-107">Attributes</span></span>

<span data-ttu-id="9f767-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="9f767-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9f767-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9f767-109">Child elements</span></span>



| <span data-ttu-id="9f767-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f767-110">Element</span></span>                                                     | <span data-ttu-id="9f767-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f767-111">Description</span></span>                                        |
|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="9f767-112">**Comando**</span><span class="sxs-lookup"><span data-stu-id="9f767-112">**Command**</span></span>](windowsribbon-element-command.md)<br/> | <span data-ttu-id="9f767-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="9f767-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9f767-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="9f767-114">Parent elements</span></span>



| <span data-ttu-id="9f767-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f767-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="9f767-116">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="9f767-116">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9f767-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f767-117">Remarks</span></span>

<span data-ttu-id="9f767-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9f767-118">Optional.</span></span>

<span data-ttu-id="9f767-119">Può verificarsi al massimo una volta per ogni elemento [**dell'applicazione**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="9f767-119">May occur at most once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="9f767-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="9f767-120">Examples</span></span>

<span data-ttu-id="9f767-121">Nell'esempio seguente viene illustrato un elemento **Application. Commands** che contiene un manifesto di comandi degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="9f767-121">The following example shows an **Application.Commands** element that contains a manifest of clipboard Commands.</span></span>


```C++
<Application.Commands>
```




```C++
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




```C++
</Application.Commands>
```



## <a name="requirements"></a><span data-ttu-id="9f767-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f767-122">Requirements</span></span>



| <span data-ttu-id="9f767-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f767-123">Requirement</span></span> | <span data-ttu-id="9f767-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9f767-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9f767-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f767-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9f767-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9f767-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9f767-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f767-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9f767-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f767-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f767-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f767-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f767-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="9f767-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)
</dt> </dl>

 

 





