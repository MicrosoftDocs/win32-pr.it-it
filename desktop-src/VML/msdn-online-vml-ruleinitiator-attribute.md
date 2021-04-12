---
title: Attributo RuleInitiator di la
description: Attributo RuleInitiator di la
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339103"
---
# <a name="vml-ruleinitiator-attribute"></a><span data-ttu-id="705b2-103">Attributo RuleInitiator di la</span><span class="sxs-lookup"><span data-stu-id="705b2-103">VML RuleInitiator Attribute</span></span>

<span data-ttu-id="705b2-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="705b2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="705b2-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="705b2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="705b2-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="705b2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="705b2-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="705b2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="705b2-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="705b2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="705b2-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="705b2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="705b2-110">Determina se verrà utilizzato un motore regole.</span><span class="sxs-lookup"><span data-stu-id="705b2-110">Determines whether a rules engine will be used.</span></span> <span data-ttu-id="705b2-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="705b2-111">Read/write.</span></span> <span data-ttu-id="705b2-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="705b2-112">**VgTriState**.</span></span>

<span data-ttu-id="705b2-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="705b2-113">**Applies To**</span></span>

[<span data-ttu-id="705b2-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="705b2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="705b2-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="705b2-115">**Tag Syntax**</span></span>

<span data-ttu-id="705b2-116"><v: *element* o:ruleinitiator = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="705b2-116"><v: *element* o:ruleinitiator=" *expression* "></span></span>

<span data-ttu-id="705b2-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="705b2-117">**Remarks**</span></span>

<span data-ttu-id="705b2-118">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="705b2-118">The default value is **False**.</span></span> <span data-ttu-id="705b2-119">Se il valore è **true**, viene usato un motore regole.</span><span class="sxs-lookup"><span data-stu-id="705b2-119">If the value is **True**, a rules engine is used.</span></span>

<span data-ttu-id="705b2-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="705b2-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="705b2-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="705b2-121">**Example**</span></span>

<span data-ttu-id="705b2-122">La forma verrà elaborata da un motore regole.</span><span class="sxs-lookup"><span data-stu-id="705b2-122">The shape will be processed by a rules engine.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 