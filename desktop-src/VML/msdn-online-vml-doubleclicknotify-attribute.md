---
title: Attributo DoubleClickNotify di la
description: Attributo DoubleClickNotify di la
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337607"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="78200-103">Attributo DoubleClickNotify di la</span><span class="sxs-lookup"><span data-stu-id="78200-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="78200-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="78200-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="78200-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="78200-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="78200-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="78200-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="78200-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="78200-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="78200-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="78200-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="78200-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="78200-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="78200-110">Invia un messaggio di evento quando si fa doppio clic su una forma.</span><span class="sxs-lookup"><span data-stu-id="78200-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="78200-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="78200-111">Read/write.</span></span> <span data-ttu-id="78200-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="78200-112">**VgTriState**.</span></span>

<span data-ttu-id="78200-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="78200-113">**Applies To**</span></span>

[<span data-ttu-id="78200-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="78200-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="78200-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="78200-115">**Tag Syntax**</span></span>

<span data-ttu-id="78200-116"><v: *element* o:doubleclicknotify = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="78200-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="78200-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="78200-117">**Remarks**</span></span>

<span data-ttu-id="78200-118">Il valore predefinito è **false**, che indica che l'evento non verrà generato.</span><span class="sxs-lookup"><span data-stu-id="78200-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="78200-119">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="78200-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="78200-120">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="78200-120">**Example**</span></span>

<span data-ttu-id="78200-121">Quando si fa doppio clic, la forma attiverà un evento di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="78200-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 