---
description: L'oggetto DivisionResult rappresenta uno snapshot dell'analisi del layout dei tratti contenuti dall'oggetto divisore. Contiene le informazioni di raggruppamento e classificazione tratto dall'analisi del layout.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Utilizzo dell'oggetto DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526887"
---
# <a name="working-with-the-divisionresult-object"></a><span data-ttu-id="7d1fa-104">Utilizzo dell'oggetto DivisionResult</span><span class="sxs-lookup"><span data-stu-id="7d1fa-104">Working with the DivisionResult Object</span></span>

<span data-ttu-id="7d1fa-105">L'oggetto **DivisionResult** rappresenta uno snapshot dell'analisi del layout dei tratti contenuti dall'oggetto **divisore** .</span><span class="sxs-lookup"><span data-stu-id="7d1fa-105">The **DivisionResult** object represents a snapshot of the layout analysis of the strokes contained by the **Divider** object.</span></span> <span data-ttu-id="7d1fa-106">Contiene le informazioni di raggruppamento e classificazione tratto dall'analisi del layout.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-106">It contains the stroke classification and grouping information from the layout analysis.</span></span>

<span data-ttu-id="7d1fa-107">È possibile ottenere informazioni dall'oggetto **DivisionResult** in base al tipo di elemento strutturale, ad esempio disegno o righe di grafia.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-107">You can get information from the **DivisionResult** object by structural element type, such as drawing or lines of handwriting.</span></span> <span data-ttu-id="7d1fa-108">L'oggetto **DivisionResult** può essere mantenuto dopo che l'oggetto **divisore** è stato eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-108">The **DivisionResult** object can persist after the **Divider** object is destroyed.</span></span> <span data-ttu-id="7d1fa-109">In automazione, questo oggetto viene chiamato oggetto [**interfaccia IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="7d1fa-109">In Automation, this object is called the [**IInkDivisionResult Interface**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="7d1fa-110">La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) dell'oggetto **DivisionResult** contiene una copia della raccolta **Strokes** nell'oggetto **divisore** al momento della creazione dell'oggetto **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="7d1fa-110">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the **DivisionResult** object contains a copy of the **Strokes** collection in the **Divider** object at the time the **DivisionResult** object was created.</span></span>

<span data-ttu-id="7d1fa-111">L'enumerazione [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) definisce i tipi di elementi strutturali riconosciuti dall'analisi del layout.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-111">The [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration defines the structural element types that the layout analysis recognizes.</span></span>

<span data-ttu-id="7d1fa-112">Il metodo [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) dell'oggetto **DivisionResult** restituisce una raccolta **DivisionUnits** che contiene tutti gli elementi strutturali di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="7d1fa-112">The [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method of the **DivisionResult** object returns a **DivisionUnits** collection that contains all structural elements of a given type.</span></span> <span data-ttu-id="7d1fa-113">Un singolo elemento strutturale è rappresentato da un oggetto **DivisionUnit** .</span><span class="sxs-lookup"><span data-stu-id="7d1fa-113">An individual structural element is represented by a **DivisionUnit** object.</span></span> <span data-ttu-id="7d1fa-114">Ogni volta che si chiama il metodo **ResultByType** , l'oggetto **DivisionResult** crea una raccolta **DivisionUnits** .</span><span class="sxs-lookup"><span data-stu-id="7d1fa-114">Each time you call the **ResultByType** method, the **DivisionResult** object creates a **DivisionUnits** collection.</span></span> <span data-ttu-id="7d1fa-115">Per ulteriori informazioni sull'oggetto **DivisionUnit** , vedere [utilizzo dell'oggetto DivisionUnit](working-with-the-divisionunit-object.md).</span><span class="sxs-lookup"><span data-stu-id="7d1fa-115">For more information about the **DivisionUnit** object, see [Working with the DivisionUnit Object](working-with-the-divisionunit-object.md).</span></span>

 

 
