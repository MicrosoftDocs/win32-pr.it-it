---
title: Attributo PreferRelative di la
description: Attributo PreferRelative di la
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046838"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="519cb-103">Attributo PreferRelative di la</span><span class="sxs-lookup"><span data-stu-id="519cb-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="519cb-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="519cb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="519cb-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="519cb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="519cb-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="519cb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="519cb-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="519cb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="519cb-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="519cb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="519cb-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="519cb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="519cb-110">Determina se le dimensioni originali di un oggetto vengono salvate dopo la riformattazione.</span><span class="sxs-lookup"><span data-stu-id="519cb-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="519cb-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="519cb-111">Read/write.</span></span> <span data-ttu-id="519cb-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="519cb-112">**VgTriState**.</span></span>

<span data-ttu-id="519cb-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="519cb-113">**Applies To**</span></span>

[<span data-ttu-id="519cb-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="519cb-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="519cb-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="519cb-115">**Tag Syntax**</span></span>

<span data-ttu-id="519cb-116"><v: *element* o:preferrelative = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="519cb-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="519cb-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="519cb-117">**Remarks**</span></span>

<span data-ttu-id="519cb-118">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="519cb-118">The default is **False**.</span></span> <span data-ttu-id="519cb-119">Se **true**, le dimensioni originali dell'oggetto verranno archiviate e tutto il ridimensionamento sarà basato su una percentuale delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="519cb-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="519cb-120">In caso contrario, ogni ridimensionamento Reimposta la scala al 100%.</span><span class="sxs-lookup"><span data-stu-id="519cb-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="519cb-121">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="519cb-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="519cb-122">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="519cb-122">**Example**</span></span>

<span data-ttu-id="519cb-123">Se la forma viene ridimensionata, le dimensioni originali non verranno archiviate.</span><span class="sxs-lookup"><span data-stu-id="519cb-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 