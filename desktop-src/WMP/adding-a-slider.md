---
title: Aggiunta di un dispositivo di scorrimento
description: Aggiunta di un dispositivo di scorrimento
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- creazione di interfacce, dispositivi di scorrimento
- Interfacce di Media Player Windows, dispositivi di scorrimento
- interfacce, dispositivi di scorrimento
- dispositivi di scorrimento nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044968"
---
# <a name="adding-a-slider"></a><span data-ttu-id="e0765-107">Aggiunta di un dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="e0765-107">Adding a Slider</span></span>

<span data-ttu-id="e0765-108">È possibile aggiungere un dispositivo di scorrimento per visualizzare la posizione corrente del supporto e consentire anche all'utente di modificare la posizione nel file multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="e0765-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="e0765-109">Prima di tutto è necessario aggiungere l'elemento **Slider** :</span><span class="sxs-lookup"><span data-stu-id="e0765-109">First you must add the **SLIDER** element:</span></span>


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="e0765-110">Viene impostato un valore massimo in base alla durata del file multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="e0765-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="e0765-111">Viene usata una bitmap di immagini Thumb minuscola che è solo un quadrato verde di 10 pixel per 10 pixel.</span><span class="sxs-lookup"><span data-stu-id="e0765-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="e0765-112">Lo sfondo del dispositivo di scorrimento sarà rosso e il primo piano sarà blu.</span><span class="sxs-lookup"><span data-stu-id="e0765-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="e0765-113">Quando l'utente trascina l'immagine del cursore in una nuova posizione e consente di passare al pulsante del mouse, il supporto viene modificato in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="e0765-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="e0765-114">Il dispositivo di scorrimento, tuttavia, non si sposta da solo a meno che non si misuri la posizione corrente con l'attributo **\_ OnChange CurrentPosition** dell'elemento **Controls** , che è incorporato nell'elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="e0765-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="e0765-115">Quando viene modificata la posizione del supporto, viene generato un evento che esegue quindi la riga di codice che modifica il valore del dispositivo di scorrimento in base alla posizione corrente del supporto.</span><span class="sxs-lookup"><span data-stu-id="e0765-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="e0765-116">Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia del dispositivo di scorrimento funzionante simile.</span><span class="sxs-lookup"><span data-stu-id="e0765-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0765-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0765-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0765-118">**Guida alla creazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="e0765-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




