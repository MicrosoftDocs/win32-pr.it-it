---
title: Testo (Windows Media Player SDK)
description: Testo
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Mobile Skins, testo
- interfacce, testo
- riferimento per interfacce, testo
- testo nelle interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873241"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="a2109-107">Testo (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="a2109-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="a2109-108">Si consiglia di usare una o più caselle di testo visualizzate nell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a2109-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="a2109-109">Ogni casella di visualizzazione di testo usata deve essere definita nel file di definizione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a2109-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="a2109-110">Se non si definisce una casella di visualizzazione di testo in questa sezione, l'interfaccia non sarà in grado di utilizzarla.</span><span class="sxs-lookup"><span data-stu-id="a2109-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="a2109-111">La sezione di testo del file di definizione dell'interfaccia personalizzata inizia con questa riga:</span><span class="sxs-lookup"><span data-stu-id="a2109-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="a2109-112">È quindi necessario aggiungere una o più righe contenenti informazioni su ognuna delle caselle di testo visualizzate nell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="a2109-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="a2109-113">È possibile usare il modello seguente per la sezione di testo del file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="a2109-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="a2109-114">È necessario utilizzare l'ordine illustrato nel modello precedente per informazioni sulla casella di visualizzazione del testo per ogni riga della sezione di testo.</span><span class="sxs-lookup"><span data-stu-id="a2109-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="a2109-115">Ogni parte della riga è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="a2109-115">Each part of the line is required.</span></span> <span data-ttu-id="a2109-116">Le sezioni seguenti descrivono ogni elemento in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="a2109-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="a2109-117">Tipo di testo</span><span class="sxs-lookup"><span data-stu-id="a2109-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="a2109-118">Posizione del testo</span><span class="sxs-lookup"><span data-stu-id="a2109-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="a2109-119">Allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="a2109-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="a2109-120">Carattere testo</span><span class="sxs-lookup"><span data-stu-id="a2109-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="a2109-121">Colore del testo</span><span class="sxs-lookup"><span data-stu-id="a2109-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="a2109-122">Per un esempio di codice di testo, vedere la [sezione di testo di esempio](sample-text-section.md).</span><span class="sxs-lookup"><span data-stu-id="a2109-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2109-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2109-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2109-124">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="a2109-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




