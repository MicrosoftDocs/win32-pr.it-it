---
title: Aggiunta del pulsante Chiudielement
description: Aggiunta del pulsante Chiudielement
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- creazione di interfacce, elemento BUTTONelement
- Windows Media Player Skin, elemento BUTTONelement
- interfacce, elemento BUTTONelement
- file di definizione dell'interfaccia, elemento BUTTONelement
- BUTTONelement (elemento)
- Elements, BUTTONelement
- creazione di interfacce, chiusura di pulsanti
- Interfacce Media Player di Windows, pulsanti Chiudi
- interfacce, pulsanti Chiudi
- file di definizione dell'interfaccia, pulsanti Chiudi
- Chiudi pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221525"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="83800-114">Aggiunta del pulsante Chiudielement</span><span class="sxs-lookup"><span data-stu-id="83800-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="83800-115">Il pulsante Chiudi è concettualmente simile al pulsante Riproduci, ma dispone di codici e colori diversi.</span><span class="sxs-lookup"><span data-stu-id="83800-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="83800-116">Inserire il codice del **pulsante** di chiusura dopo la parentesi angolare di chiusura del **pulsante** di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="83800-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="83800-117">Gli attributi seguenti vengono usati per definire il **pulsante ButtonElement** per il pulsante Chiudi:</span><span class="sxs-lookup"><span data-stu-id="83800-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="83800-118">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="83800-118">**mappingColor**</span></span>

<span data-ttu-id="83800-119">Si tratta del valore del colore dell'area nel file di grafica di mapping creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="83800-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="83800-120">In questo caso si tratta del colore rosso a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="83800-120">In this case it is the solid red color.</span></span> <span data-ttu-id="83800-121">Questo attributo è obbligatorio per qualsiasi **pulsanteelement**.</span><span class="sxs-lookup"><span data-stu-id="83800-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="83800-122">Definendo questo colore, si indica a Windows Media Player di associare questa area dei colori al codice XML di questo pulsante.</span><span class="sxs-lookup"><span data-stu-id="83800-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="83800-123">**Descrizione comando**</span><span class="sxs-lookup"><span data-stu-id="83800-123">**upToolTip**</span></span>

<span data-ttu-id="83800-124">Definisce il testo che verrà visualizzato quando l'utente passa il puntatore del mouse sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="83800-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="83800-125">Si tratta dello stesso pulsante Riproduci, ad eccezione del fatto che è denominato "close".</span><span class="sxs-lookup"><span data-stu-id="83800-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="83800-126">**onClick**</span><span class="sxs-lookup"><span data-stu-id="83800-126">**onClick**</span></span>

<span data-ttu-id="83800-127">Definisce l'evento che si verifica quando si fa clic con il mouse sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="83800-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="83800-128">Il valore di questo attributo evento è denominato gestore eventi e sarà una riga di codice Microsoft JScript o una funzione JScript in un file di testo esterno caricato dall'attributo **loadScript** di una **vista**.</span><span class="sxs-lookup"><span data-stu-id="83800-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="83800-129">In questo caso, il codice JScript chiama il metodo **Close** dell'elemento **View** usando la **visualizzazione** dell'attributo globale, che chiude la visualizzazione e arresta Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="83800-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83800-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83800-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83800-131">**Creazione del file di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="83800-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




