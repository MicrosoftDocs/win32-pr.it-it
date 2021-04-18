---
title: Attributo ConnectorType di la
description: Attributo ConnectorType di la
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299859"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="ac057-103">Attributo ConnectorType di la</span><span class="sxs-lookup"><span data-stu-id="ac057-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="ac057-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ac057-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ac057-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ac057-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ac057-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ac057-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ac057-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ac057-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ac057-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ac057-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ac057-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ac057-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ac057-110">Indica il tipo di connettore usato per l'Unione di forme.</span><span class="sxs-lookup"><span data-stu-id="ac057-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="ac057-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ac057-111">Read/write.</span></span> <span data-ttu-id="ac057-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="ac057-112">**String**.</span></span>

<span data-ttu-id="ac057-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ac057-113">**Applies To**</span></span>

[<span data-ttu-id="ac057-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="ac057-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ac057-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ac057-115">**Tag Syntax**</span></span>

<span data-ttu-id="ac057-116"><v: *element* o:ConnectorType = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ac057-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="ac057-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ac057-117">**Remarks**</span></span>

<span data-ttu-id="ac057-118">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="ac057-118">Values include:</span></span>



| <span data-ttu-id="ac057-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ac057-119">Value</span></span>    | <span data-ttu-id="ac057-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac057-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="ac057-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac057-121">none</span></span>     | <span data-ttu-id="ac057-122">Nessun connettore.</span><span class="sxs-lookup"><span data-stu-id="ac057-122">No connector.</span></span>                  |
| <span data-ttu-id="ac057-123">direttamente</span><span class="sxs-lookup"><span data-stu-id="ac057-123">straight</span></span> | <span data-ttu-id="ac057-124">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ac057-124">Default.</span></span> <span data-ttu-id="ac057-125">Un connettore lineare.</span><span class="sxs-lookup"><span data-stu-id="ac057-125">A straight connector.</span></span> |
| <span data-ttu-id="ac057-126">gomito</span><span class="sxs-lookup"><span data-stu-id="ac057-126">elbow</span></span>    | <span data-ttu-id="ac057-127">Un connettore a forma di gomito.</span><span class="sxs-lookup"><span data-stu-id="ac057-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="ac057-128">curvo</span><span class="sxs-lookup"><span data-stu-id="ac057-128">curved</span></span>   | <span data-ttu-id="ac057-129">Un connettore curvo.</span><span class="sxs-lookup"><span data-stu-id="ac057-129">A curved connector.</span></span>            |



 

<span data-ttu-id="ac057-130">Questo attributo può essere usato anche da un motore di regole di un editor grafico.</span><span class="sxs-lookup"><span data-stu-id="ac057-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="ac057-131">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="ac057-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="ac057-132">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ac057-132">**Example**</span></span>

<span data-ttu-id="ac057-133">La forma usa una linea retta come connettore.</span><span class="sxs-lookup"><span data-stu-id="ac057-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 