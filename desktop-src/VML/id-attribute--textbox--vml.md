---
title: Attributo ID (TextBox) (la)
description: Attributo ID (TextBox) (la)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872677"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="37469-103">Attributo ID (TextBox) (la)</span><span class="sxs-lookup"><span data-stu-id="37469-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="37469-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="37469-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="37469-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="37469-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="37469-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="37469-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="37469-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="37469-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="37469-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="37469-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="37469-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="37469-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="37469-110">Nome che fornisce un identificatore univoco per una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="37469-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="37469-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="37469-111">Read/write.</span></span> <span data-ttu-id="37469-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="37469-112">**String**.</span></span>

<span data-ttu-id="37469-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="37469-113">**Applies To**</span></span>

[<span data-ttu-id="37469-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="37469-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="37469-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="37469-115">**Tag Syntax**</span></span>

<span data-ttu-id="37469-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="37469-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="37469-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="37469-117">**Script Syntax**</span></span>

<span data-ttu-id="37469-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="37469-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="37469-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="37469-119">*expression*=*element*.id</span></span>

<span data-ttu-id="37469-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="37469-120">**Remarks**</span></span>

<span data-ttu-id="37469-121">Usare **ID** per fare riferimento a una casella di testo specifica.</span><span class="sxs-lookup"><span data-stu-id="37469-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="37469-122">Dopo aver creato una casella di testo e avergli assegnato un ID, è possibile usare il nome ID quando si desidera modificare la casella di testo.</span><span class="sxs-lookup"><span data-stu-id="37469-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="37469-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="37469-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="37469-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="37469-124">**Example**</span></span>

<span data-ttu-id="37469-125">La forma ha un ID TextBox denominato "TextBox".</span><span class="sxs-lookup"><span data-stu-id="37469-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 