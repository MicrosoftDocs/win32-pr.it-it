---
description: "Quando si decide quando e come usare l'oggetto divisore in un'applicazione, tenere presente quanto segue:"
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Altre considerazioni sul divisore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232478"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="ea9fe-103">Altre considerazioni sul divisore</span><span class="sxs-lookup"><span data-stu-id="ea9fe-103">Other Divider Considerations</span></span>

<span data-ttu-id="ea9fe-104">Quando si decide quando e come usare l'oggetto [**divisore**](inkdivider-class.md) in un'applicazione, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ea9fe-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="ea9fe-105">L'oggetto [**divisore**](inkdivider-class.md) è progettato per separare i disegni e i blocchi di grafia, ma non per riconoscere livelli più elevati di struttura, ad esempio tabelle o colonne.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="ea9fe-106">L'oggetto [**divisore**](inkdivider-class.md) non fornisce interfacce specifiche per la correzione dei risultati dell'analisi del layout.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="ea9fe-107">L'utilizzo del timeout e del numero di euristiche del tratto per aggiungere o rimuovere più tratti alla volta dai tratti nell'oggetto [**divisore**](inkdivider-class.md) può migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="ea9fe-108">Considerazioni sulla rianalisi</span><span class="sxs-lookup"><span data-stu-id="ea9fe-108">Reanalysis Considerations</span></span>

<span data-ttu-id="ea9fe-109">Se si sta prendendo in considerazione l'uso dell'oggetto [**divisore**](inkdivider-class.md) in un'applicazione in cui l'oggetto **divisore** potrebbe dover rianalizzare grandi quantità di input penna, tenere presente quanto segue.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="ea9fe-110">Conservazione di copie di input penna e tratti</span><span class="sxs-lookup"><span data-stu-id="ea9fe-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="ea9fe-111">Un'applicazione può tenere copie degli oggetti [**Ink**](inkdisp-class.md) e [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) per gli elementi dell'applicazione che possono essere rivisitati successivamente nella sessione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="ea9fe-112">In questo modo si elimina la necessità di rianalizzare l'oggetto **Ink** se l'utente torna all'elemento.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="ea9fe-113">Questo approccio viene compromesso dalla memoria per ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="ea9fe-114">Euristica di riduzione dei dati</span><span class="sxs-lookup"><span data-stu-id="ea9fe-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="ea9fe-115">Potrebbe essere possibile registrare i risultati dell'analisi come dati dell'applicazione e implementare l'euristica per determinare quando rianalizzare un set di tratti.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="ea9fe-116">Questa pratica ridurrebbe la necessità di analizzare di tutto l'input penna nell'applicazione tra le sessioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="ea9fe-117">Tuttavia, è necessario prestare attenzione per mantenere i limiti degli elementi strutturali o per analizzare nuovamente tutti i tratti per gli elementi interessati.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea9fe-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea9fe-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea9fe-119">**Classe InkDivider**</span><span class="sxs-lookup"><span data-stu-id="ea9fe-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="ea9fe-120">[Classe Microsoft. Ink. Divider](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ea9fe-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 
