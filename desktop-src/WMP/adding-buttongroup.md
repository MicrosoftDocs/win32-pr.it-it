---
title: Aggiunta di BUTTONGROUP
description: Aggiunta di BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- creazione di interfacce, elemento BUTTONGROUP
- Windows Media Player Skin, elemento BUTTONGROUP
- interfacce, elemento BUTTONGROUP
- file di definizione dell'interfaccia, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- elementi, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329079"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="2d195-109">Aggiunta di BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="2d195-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="2d195-110">Questo esempio usa l'elemento **ButtonGroup** per il codice nel file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="2d195-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="2d195-111">**ButtonGroup** crea un modo semplice per elaborare gli eventi del mouse senza dover calcolare le posizioni esatte sullo schermo e usa il colore anziché le coordinate x e y.</span><span class="sxs-lookup"><span data-stu-id="2d195-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="2d195-112">Per prima cosa, è necessario aggiungere i tag **ButtonGroup** al file di definizione dell'interfaccia creata.</span><span class="sxs-lookup"><span data-stu-id="2d195-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="2d195-113">Inserirli dopo gli attributi del tag del **tema** .</span><span class="sxs-lookup"><span data-stu-id="2d195-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="2d195-114">Lasciare alcune righe vuote sopra il tag di chiusura **ButtonGroup** per i pulsanti che verrà aggiunto successivamente.</span><span class="sxs-lookup"><span data-stu-id="2d195-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="2d195-115">Gli attributi seguenti vengono usati per definire **ButtonGroup**:</span><span class="sxs-lookup"><span data-stu-id="2d195-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="2d195-116">**mappingImage**</span><span class="sxs-lookup"><span data-stu-id="2d195-116">**mappingImage**</span></span>

<span data-ttu-id="2d195-117">Si tratta del nome file del file di grafica di mapping creato in precedenza, quello con i cerchi rossi e verdi.</span><span class="sxs-lookup"><span data-stu-id="2d195-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="2d195-118">Questo attributo è obbligatorio per qualsiasi **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="2d195-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="2d195-119">**hoverImage**</span><span class="sxs-lookup"><span data-stu-id="2d195-119">**hoverImage**</span></span>

<span data-ttu-id="2d195-120">Si tratta del nome file del file di immagine del passaggio del mouse creato in precedenza, quello con i due pulsanti gialli che leggono "Play" e "close".</span><span class="sxs-lookup"><span data-stu-id="2d195-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="2d195-121">Questa operazione non è obbligatoria, ma un'immagine del passaggio del mouse consente di fornire commenti e suggerimenti all'utente.</span><span class="sxs-lookup"><span data-stu-id="2d195-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d195-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d195-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d195-123">**Creazione del file di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="2d195-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




