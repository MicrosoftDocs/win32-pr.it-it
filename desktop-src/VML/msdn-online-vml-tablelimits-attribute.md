---
title: Attributo TableLimits di la
description: Attributo TableLimits di la
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727578"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="09005-103">Attributo TableLimits di la</span><span class="sxs-lookup"><span data-stu-id="09005-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="09005-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="09005-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="09005-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="09005-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="09005-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="09005-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="09005-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="09005-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="09005-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="09005-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="09005-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="09005-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="09005-110">Elenco di valori di altezza minima per ogni riga di una tabella.</span><span class="sxs-lookup"><span data-stu-id="09005-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="09005-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="09005-111">Read/write.</span></span> <span data-ttu-id="09005-112">**VgLengthArray**.</span><span class="sxs-lookup"><span data-stu-id="09005-112">**VgLengthArray**.</span></span>

<span data-ttu-id="09005-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="09005-113">**Applies To**</span></span>

[<span data-ttu-id="09005-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="09005-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="09005-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="09005-115">**Tag Syntax**</span></span>

<span data-ttu-id="09005-116"><v: *element* o:tablelimits = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="09005-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="09005-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="09005-117">**Remarks**</span></span>

<span data-ttu-id="09005-118">Usato da Microsoft PowerPoint per le tabelle native.</span><span class="sxs-lookup"><span data-stu-id="09005-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="09005-119">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="09005-119">Default value is **Null**.</span></span>

<span data-ttu-id="09005-120">Anche se il valore viene archiviato in una forma, l'attributo è utile solo quando la tabella è costituita da forme raggruppate.</span><span class="sxs-lookup"><span data-stu-id="09005-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="09005-121">Quando si aggiunge un testo alle celle della tabella, è possibile che l'altezza della riga aumenti.</span><span class="sxs-lookup"><span data-stu-id="09005-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="09005-122">L'attributo **TableLimits** archivia l'altezza della riga originale in modo che, se il testo viene eliminato, l'altezza della riga non scenderà al di sotto del valore originale.</span><span class="sxs-lookup"><span data-stu-id="09005-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="09005-123">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="09005-123">*Microsoft Office Extensions Attribute*</span></span>

 

 