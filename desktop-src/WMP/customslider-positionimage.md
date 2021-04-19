---
title: CUSTOMSLIDER. dimensione positionImage
description: L'attributo dimensione positionImage specifica o recupera la mappa immagine utilizzata per determinare l'immagine della posizione dal file di immagine da visualizzare.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- Media Player Windows CUSTOMSLIDER. dimensione positionImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324102"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="12d15-104">CUSTOMSLIDER. dimensione positionImage</span><span class="sxs-lookup"><span data-stu-id="12d15-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="12d15-105">L'attributo **dimensione positionImage** specifica o recupera la mappa immagine utilizzata per determinare l'immagine della posizione dal file di immagine da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="12d15-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="12d15-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="12d15-106">Possible Values</span></span>

<span data-ttu-id="12d15-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="12d15-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d15-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="12d15-108">Remarks</span></span>

<span data-ttu-id="12d15-109">Questo attributo è obbligatorio e deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="12d15-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="12d15-110">**Dimensione positionImage** non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="12d15-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="12d15-111">Al contrario, funge da mappa che definisce le aree selezionabili dell'immagine visualizzata.</span><span class="sxs-lookup"><span data-stu-id="12d15-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="12d15-112">L'immagine visualizzata è una delle immagini secondarie del file di immagine e rappresenta lo stato effettivo del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="12d15-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="12d15-113">Il **dimensione positionImage** include un numero di aree di scala grigie uguale al numero di queste immagini secondarie.</span><span class="sxs-lookup"><span data-stu-id="12d15-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="12d15-114">Le immagini secondarie devono avere le stesse dimensioni di **dimensione positionImage** o il dispositivo di scorrimento personalizzato non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="12d15-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="12d15-115">Non sarà possibile fare clic su un'area che non è in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="12d15-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="12d15-116">Le aree selezionabili devono essere impostate su valori di colore che variano uniformemente nello spettro della scala grigia da nero a bianco, in cui la prima area è nera pura e l'ultima area è bianca.</span><span class="sxs-lookup"><span data-stu-id="12d15-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="12d15-117">I valori dei colori di ogni area successiva devono essere incrementati di un valore uguale a 255 diviso per il numero totale di aree meno uno, arrotondando al numero intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="12d15-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="12d15-118">Se ad esempio sono presenti sei aree, l'incremento è 51 (255 diviso per 5) e i sei valori della scala di grigi sarebbero 0, 51, 102, 153, 204 e 255.</span><span class="sxs-lookup"><span data-stu-id="12d15-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="12d15-119">I valori esadecimali dei colori per le sei aree sono quindi \# 000000, \# 333333, \# 666666, \# 999999, \# cccccc e \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="12d15-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="12d15-120">In questo modo, le aree avranno una sequenza dettata dai valori dei colori della scala grigia e questa sequenza corrisponderà alla sequenza di immagini secondarie nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="12d15-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="12d15-121">Quando si fa clic su una delle aree, viene visualizzata l'immagine secondaria corrispondente e il **valore** del dispositivo di scorrimento personalizzato viene aggiornato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="12d15-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="12d15-122">I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="12d15-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="12d15-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="12d15-123">Examples</span></span>

<span data-ttu-id="12d15-124">Di seguito è riportato un esempio di un dispositivo di scorrimento **dimensione positionImage** personalizzato.</span><span class="sxs-lookup"><span data-stu-id="12d15-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="12d15-125">L'immagine corrispondente è illustrata nella sezione esempio della proprietà **Image** .</span><span class="sxs-lookup"><span data-stu-id="12d15-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![immagine di dimensione positionImage di esempio](images/dialmap.png)

<span data-ttu-id="12d15-127">Il codice seguente illustra l'uso degli attributi **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="12d15-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

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
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="12d15-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12d15-128">Requirements</span></span>



| <span data-ttu-id="12d15-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d15-129">Requirement</span></span> | <span data-ttu-id="12d15-130">Valore</span><span class="sxs-lookup"><span data-stu-id="12d15-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="12d15-131">Versione</span><span class="sxs-lookup"><span data-stu-id="12d15-131">Version</span></span><br/> | <span data-ttu-id="12d15-132">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="12d15-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12d15-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12d15-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d15-134">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="12d15-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="12d15-135">**CUSTOMSLIDER. image**</span><span class="sxs-lookup"><span data-stu-id="12d15-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





