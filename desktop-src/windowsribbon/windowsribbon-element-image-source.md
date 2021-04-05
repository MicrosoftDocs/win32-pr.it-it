---
title: Proprietà Image. Source
description: Rappresenta il percorso della directory di un'immagine.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Proprietà Image. Source-barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740999"
---
# <a name="imagesource-property"></a><span data-ttu-id="e777f-104">Proprietà Image. Source</span><span class="sxs-lookup"><span data-stu-id="e777f-104">Image.Source property</span></span>

<span data-ttu-id="e777f-105">Rappresenta il percorso della directory di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e777f-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="e777f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e777f-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="e777f-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="e777f-107">Attributes</span></span>

<span data-ttu-id="e777f-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="e777f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e777f-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e777f-109">Child elements</span></span>

<span data-ttu-id="e777f-110">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="e777f-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e777f-111">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e777f-111">Parent elements</span></span>



| <span data-ttu-id="e777f-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="e777f-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="e777f-113">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="e777f-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e777f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e777f-114">Remarks</span></span>

<span data-ttu-id="e777f-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e777f-115">Optional.</span></span>

<span data-ttu-id="e777f-116">Può essere presente al massimo una volta per ogni [**immagine**](windowsribbon-element-image.md).</span><span class="sxs-lookup"><span data-stu-id="e777f-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="e777f-117">Questo elemento contiene un valore di tipo *xs: anyURI* o qualsiasi sequenza di caratteri che rappresenta un Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="e777f-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="e777f-118">Il valore URI è un percorso di directory assoluto o relativo (al file di markup della barra multifunzione) di una risorsa immagine di tipo bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="e777f-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="e777f-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="e777f-119">Examples</span></span>

<span data-ttu-id="e777f-120">Nell'esempio di codice seguente viene illustrato il markup necessario per dichiarare, tramite un set di elementi [**immagine**](windowsribbon-element-image.md) , una raccolta di risorse immagine progettate per supportare quattro impostazioni DPI dello schermo specifiche.</span><span class="sxs-lookup"><span data-stu-id="e777f-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="e777f-121">La proprietà **Image. Source** viene utilizzata per specificare il percorso della risorsa immagine.</span><span class="sxs-lookup"><span data-stu-id="e777f-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="e777f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e777f-122">Requirements</span></span>



| <span data-ttu-id="e777f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e777f-123">Requirement</span></span> | <span data-ttu-id="e777f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e777f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e777f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e777f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e777f-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e777f-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e777f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e777f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e777f-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e777f-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





