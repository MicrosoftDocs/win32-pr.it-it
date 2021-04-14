---
title: Proprietà Command. SmallImages
description: Rappresenta un contenitore di immagini; in questo caso, immagini di piccole dimensioni.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Barra multifunzione di Windows Command. SmallImages
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18556cf519c21b01c3e80b63cbfc9cdf9d7d153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478623"
---
# <a name="commandsmallimages-property"></a><span data-ttu-id="40b82-104">Proprietà Command. SmallImages</span><span class="sxs-lookup"><span data-stu-id="40b82-104">Command.SmallImages property</span></span>

<span data-ttu-id="40b82-105">Rappresenta un contenitore di immagini; in questo caso, immagini di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="40b82-105">Represents a container of images; in this case, small images.</span></span>

## <a name="usage"></a><span data-ttu-id="40b82-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="40b82-106">Usage</span></span>

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
```

## <a name="attributes"></a><span data-ttu-id="40b82-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="40b82-107">Attributes</span></span>

<span data-ttu-id="40b82-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="40b82-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="40b82-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="40b82-109">Child elements</span></span>



| <span data-ttu-id="40b82-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="40b82-110">Element</span></span>                                                 | <span data-ttu-id="40b82-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40b82-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="40b82-112">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="40b82-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="40b82-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="40b82-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="40b82-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="40b82-114">Parent elements</span></span>



| <span data-ttu-id="40b82-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="40b82-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="40b82-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="40b82-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="40b82-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="40b82-117">Remarks</span></span>

<span data-ttu-id="40b82-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="40b82-118">Optional.</span></span>

<span data-ttu-id="40b82-119">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="40b82-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="40b82-120">Le risorse di immagine devono essere conformi al formato grafico bitmap standard (BMP) usato in Windows.</span><span class="sxs-lookup"><span data-stu-id="40b82-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="40b82-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="40b82-121">Examples</span></span>

<span data-ttu-id="40b82-122">Nell'esempio seguente viene illustrato il markup di base per [**SplitButton**](windowsribbon-element-splitbutton.md) con un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="40b82-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="40b82-123">Questa sezione di codice mostra le dichiarazioni dei comandi [**SplitButton**](windowsribbon-element-splitbutton.md) e [**MenuGroup**](windowsribbon-element-menugroup.md) con una risorsa immagine grande e una piccola.</span><span class="sxs-lookup"><span data-stu-id="40b82-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="40b82-124">Viene anche dichiarato un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="40b82-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a><span data-ttu-id="40b82-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40b82-125">Requirements</span></span>



| <span data-ttu-id="40b82-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="40b82-126">Requirement</span></span> | <span data-ttu-id="40b82-127">Valore</span><span class="sxs-lookup"><span data-stu-id="40b82-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="40b82-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40b82-128">Minimum supported client</span></span><br/> | <span data-ttu-id="40b82-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="40b82-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="40b82-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40b82-130">Minimum supported server</span></span><br/> | <span data-ttu-id="40b82-131">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="40b82-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40b82-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40b82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b82-133">Specifica delle risorse dell'immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="40b82-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="40b82-134">Interfaccia utente \_ pkey \_ smallImage</span><span class="sxs-lookup"><span data-stu-id="40b82-134">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





