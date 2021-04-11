---
title: Stato (Windows Media Player SDK)
description: Stato
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Interfacce di Windows Media Player Mobile, visualizzazione dello stato
- interfacce, visualizzazione stato
- informazioni di riferimento per Skins, status display
- visualizzazione dello stato in interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047685"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="04016-107">Stato (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="04016-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="04016-108">Si consiglia di usare una visualizzazione dello stato nell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="04016-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="04016-109">In tal caso, l'elemento status deve essere definito nel file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="04016-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="04016-110">In alternativa, è possibile visualizzare queste informazioni anche usando l'attributo status nell'elemento di testo.</span><span class="sxs-lookup"><span data-stu-id="04016-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="04016-111">La sezione stato del file di definizione dell'interfaccia personalizzata inizia con questa riga:</span><span class="sxs-lookup"><span data-stu-id="04016-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="04016-112">È quindi necessario aggiungere una o più righe che contengono informazioni sulla visualizzazione dello stato nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="04016-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="04016-113">È possibile usare il modello seguente per la sezione stato del file di definizione dell'interfaccia utente:</span><span class="sxs-lookup"><span data-stu-id="04016-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="04016-114">È necessario usare l'ordine illustrato nel modello precedente per informazioni sullo stato di visualizzazione per ogni riga nella sezione stato.</span><span class="sxs-lookup"><span data-stu-id="04016-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="04016-115">Ogni parte della riga è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="04016-115">Each part of the line is required.</span></span> <span data-ttu-id="04016-116">Le sezioni seguenti descrivono ogni elemento:</span><span class="sxs-lookup"><span data-stu-id="04016-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="04016-117">Stato</span><span class="sxs-lookup"><span data-stu-id="04016-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="04016-118">Percorso stato</span><span class="sxs-lookup"><span data-stu-id="04016-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="04016-119">Allineamento stato</span><span class="sxs-lookup"><span data-stu-id="04016-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="04016-120">Carattere stato</span><span class="sxs-lookup"><span data-stu-id="04016-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="04016-121">Colore di stato</span><span class="sxs-lookup"><span data-stu-id="04016-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="04016-122">Per un esempio di codice di stato, vedere la [sezione Sample status](sample-status-section.md).</span><span class="sxs-lookup"><span data-stu-id="04016-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04016-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04016-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04016-124">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="04016-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




