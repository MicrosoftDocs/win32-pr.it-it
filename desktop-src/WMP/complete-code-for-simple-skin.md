---
title: Completa il codice per interfaccia semplice
description: Completa il codice per interfaccia semplice
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- creazione di interfacce, esempi di codice
- Windows Media Player Skin, esempi di codice
- interfacce, esempi di codice
- file di definizione dell'interfaccia, esempi di codice
- creazione di interfacce, esempi
- Windows Media Player Skin, esempi
- interfacce, esempi
- file di definizione dell'interfaccia, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856442"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="b7acc-111">Completa il codice per interfaccia semplice</span><span class="sxs-lookup"><span data-stu-id="b7acc-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="b7acc-112">Ecco il codice completo per la prima interfaccia di esempio:</span><span class="sxs-lookup"><span data-stu-id="b7acc-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="b7acc-113">A questo punto, tutti i componenti sono stati assemblati.</span><span class="sxs-lookup"><span data-stu-id="b7acc-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="b7acc-114">Creare un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="b7acc-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="b7acc-115">Questo file compresso contiene il file di definizione dell'interfaccia personalizzata, le bitmap e tutti i file multimediali digitali che si desidera includere.</span><span class="sxs-lookup"><span data-stu-id="b7acc-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="b7acc-116">Rinominare il file in modo che disponga di un'estensione di file WMZ.</span><span class="sxs-lookup"><span data-stu-id="b7acc-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="b7acc-117">Quindi, facendo doppio clic sull'interfaccia compressa verrà avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b7acc-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="b7acc-118">Nella sezione degli esempi dell'SDK è possibile visualizzare un'interfaccia semplice e funzionante simile.</span><span class="sxs-lookup"><span data-stu-id="b7acc-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7acc-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7acc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7acc-120">**Creazione del file di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="b7acc-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




