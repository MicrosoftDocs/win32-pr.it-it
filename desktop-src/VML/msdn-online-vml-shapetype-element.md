---
title: Elemento TipoForma di la
description: Elemento TipoForma di la
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223925"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="77188-103">Elemento TipoForma di la</span><span class="sxs-lookup"><span data-stu-id="77188-103">VML ShapeType Element</span></span>

<span data-ttu-id="77188-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="77188-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="77188-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="77188-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="77188-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="77188-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="77188-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="77188-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="77188-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="77188-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="77188-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="77188-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="77188-110">Definisce una forma che può essere utilizzata per creare altre forme.</span><span class="sxs-lookup"><span data-stu-id="77188-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="77188-111">L'attributo seguente modifica un **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="77188-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="77188-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="77188-112">Attribute</span></span>                                      | <span data-ttu-id="77188-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77188-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="77188-114">Master</span><span class="sxs-lookup"><span data-stu-id="77188-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="77188-115">Determina se un **TipoForma** è un elemento Master.</span><span class="sxs-lookup"><span data-stu-id="77188-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="77188-116">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="77188-116">**Remarks**</span></span>

<span data-ttu-id="77188-117">**TipoForma** è identico all'elemento **Shape** con la differenza che non può fare riferimento a un altro elemento **TipoForma** .</span><span class="sxs-lookup"><span data-stu-id="77188-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="77188-118">Quando un elemento **Shape** fa riferimento a un **TipoForma**, la **forma** può duplicare alcune delle proprietà che sono già state specificate in **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="77188-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="77188-119">In questi casi, gli attributi nella **forma** eseguono l'override di quelli di **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="77188-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="77188-120">L'attributo **Type** non può essere utilizzato con **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="77188-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="77188-121">Gli attributi di posizionamento CSS (ad esempio **Top**, **Left** e così via) non vengono passati a una **forma** da un **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="77188-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="77188-122">Per usare questo elemento, creare un **TipoForma** con un attributo [ID](id-attribute--vml.md) specifico.</span><span class="sxs-lookup"><span data-stu-id="77188-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="77188-123">Creare quindi una **forma** e fare riferimento a **TipoForma** con l'attributo **Type** .</span><span class="sxs-lookup"><span data-stu-id="77188-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="77188-124">Per ulteriori informazioni, vedere l'attributo [Type](type-attribute--shape--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="77188-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 