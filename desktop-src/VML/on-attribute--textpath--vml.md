---
title: Attributo on (TextPath) (la)
description: Attributo on (TextPath) (la)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517091"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="8b17a-103">Attributo on (TextPath) (la)</span><span class="sxs-lookup"><span data-stu-id="8b17a-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="8b17a-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8b17a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8b17a-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="8b17a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8b17a-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="8b17a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8b17a-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="8b17a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8b17a-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8b17a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8b17a-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8b17a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8b17a-110">Definisce se il testo viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8b17a-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="8b17a-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8b17a-111">Read/write.</span></span> <span data-ttu-id="8b17a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="8b17a-112">**VgTriState**.</span></span>

<span data-ttu-id="8b17a-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="8b17a-113">**Applies To**</span></span>

[<span data-ttu-id="8b17a-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="8b17a-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="8b17a-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="8b17a-115">**Tag Syntax**</span></span>

<span data-ttu-id="8b17a-116"><v: *element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8b17a-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="8b17a-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="8b17a-117">**Script Syntax**</span></span>

<span data-ttu-id="8b17a-118">*element* . on = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="8b17a-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="8b17a-119">*espressione* = *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="8b17a-119">*expression*=*element*.on</span></span>

<span data-ttu-id="8b17a-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="8b17a-120">**Remarks**</span></span>

<span data-ttu-id="8b17a-121">L'impostazione predefinita è **False**.</span><span class="sxs-lookup"><span data-stu-id="8b17a-121">Default is **False**.</span></span> <span data-ttu-id="8b17a-122">Questo valore deve essere impostato su **true** per visualizzare il testo in un percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="8b17a-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="8b17a-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="8b17a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8b17a-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="8b17a-124">**Example**</span></span>

<span data-ttu-id="8b17a-125">Verrà visualizzato il testo sul percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="8b17a-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 