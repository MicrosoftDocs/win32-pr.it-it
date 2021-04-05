---
title: Attributo ConnectType di la
description: Attributo ConnectType di la
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117774"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="9d341-103">Attributo ConnectType di la</span><span class="sxs-lookup"><span data-stu-id="9d341-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="9d341-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9d341-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9d341-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9d341-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9d341-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9d341-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9d341-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9d341-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9d341-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9d341-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9d341-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9d341-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9d341-110">Definisce il tipo di punti di connessione utilizzati per il collegamento di forme ad altre forme.</span><span class="sxs-lookup"><span data-stu-id="9d341-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="9d341-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9d341-111">Read/write.</span></span> <span data-ttu-id="9d341-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="9d341-112">**String**.</span></span>

<span data-ttu-id="9d341-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="9d341-113">**Applies To**</span></span>

[<span data-ttu-id="9d341-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="9d341-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="9d341-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="9d341-115">**Tag Syntax**</span></span>

<span data-ttu-id="9d341-116"><v: *element* o:connecttype = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9d341-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="9d341-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="9d341-117">**Remarks**</span></span>

<span data-ttu-id="9d341-118">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="9d341-118">Values include:</span></span>



| <span data-ttu-id="9d341-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9d341-119">Value</span></span>    | <span data-ttu-id="9d341-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d341-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d341-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9d341-121">none</span></span>     | <span data-ttu-id="9d341-122">Nessun sito di connessione.</span><span class="sxs-lookup"><span data-stu-id="9d341-122">No connection sites.</span></span> <span data-ttu-id="9d341-123">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9d341-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="9d341-124">rect</span><span class="sxs-lookup"><span data-stu-id="9d341-124">rect</span></span>     | <span data-ttu-id="9d341-125">Quattro punti di connessione standard in ai punti medi dei lati superiore, inferiore, sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="9d341-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="9d341-126">segmenti</span><span class="sxs-lookup"><span data-stu-id="9d341-126">segments</span></span> | <span data-ttu-id="9d341-127">Vengono utilizzati i punti di modifica della forma.</span><span class="sxs-lookup"><span data-stu-id="9d341-127">The edit points of the shape are used.</span></span> <span data-ttu-id="9d341-128">I punti di modifica sono i punti neri in un editor grafico utilizzati per selezionare parti di una forma.</span><span class="sxs-lookup"><span data-stu-id="9d341-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="9d341-129">custom</span><span class="sxs-lookup"><span data-stu-id="9d341-129">custom</span></span>   | <span data-ttu-id="9d341-130">Matrice personalizzata di percorsi di connessione.</span><span class="sxs-lookup"><span data-stu-id="9d341-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="9d341-131">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="9d341-131">*Microsoft Office Extensions Attribute*</span></span>

 

 