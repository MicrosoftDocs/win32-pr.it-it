---
title: Attributo stringa la
description: Attributo stringa la
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399293"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="cc541-103">Attributo stringa la</span><span class="sxs-lookup"><span data-stu-id="cc541-103">VML String Attribute</span></span>

<span data-ttu-id="cc541-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cc541-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cc541-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="cc541-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cc541-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="cc541-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cc541-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="cc541-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cc541-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cc541-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cc541-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cc541-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cc541-110">Definisce il testo del percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="cc541-110">Defines the text of the text path.</span></span> <span data-ttu-id="cc541-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cc541-111">Read/write.</span></span> <span data-ttu-id="cc541-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="cc541-112">**String**.</span></span>

<span data-ttu-id="cc541-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="cc541-113">**Applies To**</span></span>

[<span data-ttu-id="cc541-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="cc541-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="cc541-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="cc541-115">**Tag Syntax**</span></span>

<span data-ttu-id="cc541-116"><v: *element* String = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="cc541-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="cc541-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="cc541-117">**Script Syntax**</span></span>

<span data-ttu-id="cc541-118">*element* . String = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="cc541-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="cc541-119">*espressione* = *element*. String</span><span class="sxs-lookup"><span data-stu-id="cc541-119">*expression*=*element*.string</span></span>

<span data-ttu-id="cc541-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="cc541-120">**Remarks**</span></span>

<span data-ttu-id="cc541-121">È necessario assegnare una stringa di testo per visualizzare il testo in un percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="cc541-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="cc541-122">Attributo standard la</span><span class="sxs-lookup"><span data-stu-id="cc541-122">VML Standard Attribute</span></span>

<span data-ttu-id="cc541-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="cc541-123">**Example**</span></span>

<span data-ttu-id="cc541-124">La stringa che verrà visualizzata è "la Text".</span><span class="sxs-lookup"><span data-stu-id="cc541-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 