---
title: Attributo la V-same-Letter-Heights
description: Attributo la V-same-Letter-Heights
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727762"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="3be82-103">Attributo la V-same-Letter-Heights</span><span class="sxs-lookup"><span data-stu-id="3be82-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="3be82-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3be82-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3be82-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3be82-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3be82-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3be82-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3be82-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3be82-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3be82-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3be82-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3be82-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3be82-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3be82-110">Determina se tutte le lettere saranno della stessa altezza indipendentemente dal caso iniziale.</span><span class="sxs-lookup"><span data-stu-id="3be82-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="3be82-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3be82-111">Read/write.</span></span> <span data-ttu-id="3be82-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="3be82-112">**VgTriState**.</span></span>

<span data-ttu-id="3be82-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3be82-113">**Applies To**</span></span>

[<span data-ttu-id="3be82-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="3be82-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="3be82-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3be82-115">**Tag Syntax**</span></span>

<span data-ttu-id="3be82-116"><v: *elemento* Style = "v-same-Letter-Heights: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3be82-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="3be82-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="3be82-117">**Script Syntax**</span></span>

<span data-ttu-id="3be82-118">*element* . Style. v-same-Letter-Heights = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="3be82-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="3be82-119">*espressione* = *element*. Style. v-same-Letter-Heights</span><span class="sxs-lookup"><span data-stu-id="3be82-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="3be82-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3be82-120">**Remarks**</span></span>

<span data-ttu-id="3be82-121">Se **true**, le lettere minuscole vengono allungate all'altezza delle lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="3be82-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="3be82-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="3be82-122">The default value is **False**.</span></span>

<span data-ttu-id="3be82-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="3be82-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3be82-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3be82-124">**Example**</span></span>

<span data-ttu-id="3be82-125">Tutte le lettere saranno della stessa altezza, indipendentemente dalla distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3be82-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 