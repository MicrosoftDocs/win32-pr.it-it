---
title: Creazione di dispositivi di scorrimento personalizzati
description: Creazione di dispositivi di scorrimento personalizzati
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- creazione di interfacce, dispositivi di scorrimento
- Interfacce di Media Player Windows, dispositivi di scorrimento
- interfacce, dispositivi di scorrimento
- dispositivi di scorrimento nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515913"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="35f16-107">Creazione di dispositivi di scorrimento personalizzati</span><span class="sxs-lookup"><span data-stu-id="35f16-107">Creating Custom Sliders</span></span>

<span data-ttu-id="35f16-108">È possibile creare dispositivi di scorrimento personalizzati in qualsiasi forma desiderata.</span><span class="sxs-lookup"><span data-stu-id="35f16-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="35f16-109">Per questo esempio viene scelta una semplice striscia, ma la forma effettiva può essere qualsiasi elemento.</span><span class="sxs-lookup"><span data-stu-id="35f16-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="35f16-110">Ecco il codice per l'elemento **CUSTOMSLIDER** :</span><span class="sxs-lookup"><span data-stu-id="35f16-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="35f16-111">In questo modo viene impostato un valore iniziale per il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="35f16-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="35f16-112">Vengono introdotte due nuove bitmap.</span><span class="sxs-lookup"><span data-stu-id="35f16-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="35f16-113">Una è la bitmap in scala di grigi (slider.bmp) che definisce i valori che verranno usati quando si fa clic su di esso e l'altro (slider.bmp) che determina quale immagine verrà visualizzata quando si fa clic su una particolare parte della scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="35f16-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="35f16-114">Il valore iniziale viene determinato ascoltando il volume con wmpprop e quindi il volume può essere modificato quando l'utente fa clic su una parte del dispositivo di scorrimento che attiva una modifica nel valore.</span><span class="sxs-lookup"><span data-stu-id="35f16-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="35f16-115">Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia del dispositivo di scorrimento funzionante simile.</span><span class="sxs-lookup"><span data-stu-id="35f16-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35f16-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35f16-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35f16-117">**Guida alla creazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="35f16-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




