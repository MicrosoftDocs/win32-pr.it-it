---
title: Attributo Font-Family la
description: Attributo Font-Family la
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047338"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="e0569-103">Attributo Font-Family la</span><span class="sxs-lookup"><span data-stu-id="e0569-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="e0569-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e0569-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e0569-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e0569-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e0569-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e0569-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e0569-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e0569-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e0569-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e0569-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e0569-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e0569-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e0569-110">Definisce la famiglia del tipo di carattere TextPath.</span><span class="sxs-lookup"><span data-stu-id="e0569-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="e0569-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e0569-111">Read/write.</span></span> <span data-ttu-id="e0569-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="e0569-112">**String**.</span></span>

<span data-ttu-id="e0569-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e0569-113">**Applies To**</span></span>

[<span data-ttu-id="e0569-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="e0569-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e0569-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e0569-115">**Tag Syntax**</span></span>

<span data-ttu-id="e0569-116"><v: *element* Style = "font-family: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e0569-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="e0569-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e0569-117">**Script Syntax**</span></span>

<span data-ttu-id="e0569-118">*element* . Style. FontFamily = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e0569-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="e0569-119">*espressione* = *element*. Style. FontFamily</span><span class="sxs-lookup"><span data-stu-id="e0569-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="e0569-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e0569-120">**Remarks**</span></span>

<span data-ttu-id="e0569-121">Definisce il nome del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e0569-121">Defines the font name.</span></span> <span data-ttu-id="e0569-122">È possibile usare nomi specifici, ad esempio Arial, o tipi generici, ad esempio Serif, sans-serif, corsia, Fantasy o monospace.</span><span class="sxs-lookup"><span data-stu-id="e0569-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="e0569-123">I valori corrispondono agli attributi di stile HTML standard.</span><span class="sxs-lookup"><span data-stu-id="e0569-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="e0569-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e0569-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e0569-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e0569-125">**Example**</span></span>

<span data-ttu-id="e0569-126">La famiglia di caratteri del testo è Arial.</span><span class="sxs-lookup"><span data-stu-id="e0569-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 