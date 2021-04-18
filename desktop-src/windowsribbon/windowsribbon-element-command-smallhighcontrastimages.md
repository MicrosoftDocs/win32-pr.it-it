---
title: Proprietà Command. SmallHighContrastImages
description: Rappresenta un contenitore di immagini; in questo caso, immagini di piccole dimensioni da usare con impostazioni di sistema a contrasto elevato.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- Barra multifunzione di Windows Command. SmallHighContrastImages
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56291ad4e56e5f941fe4cb2790ac6afab27ad67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302314"
---
# <a name="commandsmallhighcontrastimages-property"></a><span data-ttu-id="8d87e-104">Proprietà Command. SmallHighContrastImages</span><span class="sxs-lookup"><span data-stu-id="8d87e-104">Command.SmallHighContrastImages property</span></span>

<span data-ttu-id="8d87e-105">Rappresenta un contenitore di immagini; in questo caso, immagini di piccole dimensioni da usare con impostazioni di sistema a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="8d87e-105">Represents a container of images; in this case, small images for use with high-contrast system settings.</span></span>

## <a name="usage"></a><span data-ttu-id="8d87e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8d87e-106">Usage</span></span>

``` syntax
<Command.SmallHighContrastImages>
  child elements
</Command.SmallHighContrastImages>
```

## <a name="attributes"></a><span data-ttu-id="8d87e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="8d87e-107">Attributes</span></span>

<span data-ttu-id="8d87e-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="8d87e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8d87e-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8d87e-109">Child elements</span></span>



| <span data-ttu-id="8d87e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d87e-110">Element</span></span>                                                 | <span data-ttu-id="8d87e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d87e-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="8d87e-112">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="8d87e-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="8d87e-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="8d87e-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8d87e-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8d87e-114">Parent elements</span></span>



| <span data-ttu-id="8d87e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d87e-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="8d87e-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="8d87e-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8d87e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d87e-117">Remarks</span></span>

<span data-ttu-id="8d87e-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8d87e-118">Optional.</span></span>

<span data-ttu-id="8d87e-119">Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="8d87e-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="8d87e-120">Le risorse di immagine devono essere conformi al formato grafico bitmap standard (BMP) usato in Windows.</span><span class="sxs-lookup"><span data-stu-id="8d87e-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="8d87e-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="8d87e-121">Examples</span></span>

<span data-ttu-id="8d87e-122">Nell'esempio seguente viene illustrato il markup di base per [**SplitButton**](windowsribbon-element-splitbutton.md) con un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="8d87e-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="8d87e-123">In questa sezione del codice vengono illustrate le dichiarazioni di comando [**SplitButton**](windowsribbon-element-splitbutton.md) e [**MenuGroup**](windowsribbon-element-menugroup.md) con risorse di immagine a contrasto elevato grandi e piccole.</span><span class="sxs-lookup"><span data-stu-id="8d87e-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with large and small high contrast image resources.</span></span> <span data-ttu-id="8d87e-124">Viene anche dichiarato un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="8d87e-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8d87e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d87e-125">Requirements</span></span>



| <span data-ttu-id="8d87e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d87e-126">Requirement</span></span> | <span data-ttu-id="8d87e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8d87e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8d87e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d87e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d87e-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8d87e-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8d87e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d87e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d87e-131">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d87e-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d87e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d87e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d87e-133">Specifica delle risorse dell'immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="8d87e-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="8d87e-134">Interfaccia utente \_ pkey \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="8d87e-134">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





