---
title: Attributo della classe la
description: Attributo della classe la
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963247"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="28521-103">Attributo della classe la</span><span class="sxs-lookup"><span data-stu-id="28521-103">VML Class Attribute</span></span>

<span data-ttu-id="28521-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="28521-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="28521-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="28521-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="28521-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="28521-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="28521-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="28521-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="28521-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="28521-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="28521-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="28521-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="28521-110">Fa riferimento a una definizione di uno stile CSS.</span><span class="sxs-lookup"><span data-stu-id="28521-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="28521-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="28521-111">Read/write.</span></span> <span data-ttu-id="28521-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="28521-112">**String**.</span></span>

<span data-ttu-id="28521-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="28521-113">**Applies To**</span></span>

[<span data-ttu-id="28521-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="28521-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="28521-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="28521-115">**Tag Syntax**</span></span>

<span data-ttu-id="28521-116"><v: *element* class = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="28521-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="28521-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="28521-117">**Script Syntax**</span></span>

<span data-ttu-id="28521-118">*element* . NomeClasse = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="28521-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="28521-119">*espressione* = *element*. NomeClasse</span><span class="sxs-lookup"><span data-stu-id="28521-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="28521-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="28521-120">**Remarks**</span></span>

<span data-ttu-id="28521-121">L'attributo della **classe** è simile all'attributo della **classe** HTML standard usato con i fogli di stile CSS.</span><span class="sxs-lookup"><span data-stu-id="28521-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="28521-122">Si noti che **NomeClasse** viene usato al posto della **classe** per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="28521-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="28521-123">Si noti inoltre che, per gli script, è possibile leggere solo **NomeClasse** ; Se si modifica il valore di **NomeClasse** , il rendering della forma non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="28521-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="28521-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="28521-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="28521-125">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="28521-125">**See Also**</span></span>

[<span data-ttu-id="28521-126">Con forme</span><span class="sxs-lookup"><span data-stu-id="28521-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="28521-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="28521-127">**Example**</span></span>

<span data-ttu-id="28521-128">Viene creata una classe per **Width** con lo stile</span><span class="sxs-lookup"><span data-stu-id="28521-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="28521-129">Viene quindi fatto riferimento alla larghezza includendo lo stile.</span><span class="sxs-lookup"><span data-stu-id="28521-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="28521-130">Si noti che la larghezza andheight non è definita nell'attributo **Style** , ma verrà definita dallo stile.</span><span class="sxs-lookup"><span data-stu-id="28521-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="28521-131">Si noti che la **classe** si applica solo agli attributi di tipo CSS.</span><span class="sxs-lookup"><span data-stu-id="28521-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 