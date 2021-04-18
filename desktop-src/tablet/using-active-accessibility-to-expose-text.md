---
description: Panoramica dell'utilizzo di Active Accessibility per esporre il testo.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Utilizzo di Active Accessibility per esporre il testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306723"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="e674d-103">Utilizzo di Active Accessibility per esporre il testo</span><span class="sxs-lookup"><span data-stu-id="e674d-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="e674d-104">Le applicazioni possono utilizzare Microsoft Active Accessibility per esporre il testo.</span><span class="sxs-lookup"><span data-stu-id="e674d-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="e674d-105">Tuttavia, l'interfaccia [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definita da versioni precedenti di Active Accessibility non è ottimizzata per l'esposizione di grandi quantità di testo RTF.</span><span class="sxs-lookup"><span data-stu-id="e674d-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="e674d-106">Le versioni successive definiscono le interfacce ottimizzate per esporre grandi quantità di testo e attributi testuali.</span><span class="sxs-lookup"><span data-stu-id="e674d-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="e674d-107">Per esporre il testo di grandi quantità, creare oggetti Component Object Model (COM) distinti che supportano [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), o elementi figlio, per rappresentare ogni esecuzione di testo.</span><span class="sxs-lookup"><span data-stu-id="e674d-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="e674d-108">Un'esecuzione è una riga, o parte di una linea, che condivide la stessa formattazione.</span><span class="sxs-lookup"><span data-stu-id="e674d-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="e674d-109">Active Accessibility espone solo il testo e il relativo percorso, ma non ha alcun meccanismo per esporre la formattazione del testo.</span><span class="sxs-lookup"><span data-stu-id="e674d-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="e674d-110">Nonostante queste limitazioni, alcuni programmi utilizzano Active Accessibility per esporre il testo.</span><span class="sxs-lookup"><span data-stu-id="e674d-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="e674d-111">Ad esempio, Microsoft Internet Explorer e Microsoft Visual Studio utilizzano entrambi Active Accessibility per esporre grandi quantità di testo.</span><span class="sxs-lookup"><span data-stu-id="e674d-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="e674d-112">Per ulteriori informazioni sull'esposizione del testo tramite Active Accessibility, vedere [accessibilità](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="e674d-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
