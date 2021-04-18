---
title: TEXT. Value
description: L'attributo value specifica o Recupera il testo visualizzato nel controllo di testo.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- Media Player di Windows TEXT. Value
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327482"
---
# <a name="textvalue"></a><span data-ttu-id="8442d-104">TEXT. Value</span><span class="sxs-lookup"><span data-stu-id="8442d-104">TEXT.value</span></span>

<span data-ttu-id="8442d-105">L'attributo **value** specifica o Recupera il testo visualizzato nel controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="8442d-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="8442d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8442d-106">Possible Values</span></span>

<span data-ttu-id="8442d-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8442d-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8442d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8442d-108">Remarks</span></span>

<span data-ttu-id="8442d-109">Se la larghezza del controllo di testo non è sufficiente per contenere il testo specificato, il testo viene ritagliato e vengono visualizzati i puntini di sospensione per illustrare il fatto.</span><span class="sxs-lookup"><span data-stu-id="8442d-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="8442d-110">Se l'attributo **ToolTip** non è stato impostato, il testo completo verrà visualizzato come descrizione comando quando il cursore passa il puntatore del mouse sul controllo.</span><span class="sxs-lookup"><span data-stu-id="8442d-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="8442d-111">Se non viene specificata una larghezza, la larghezza predefinita per il controllo corrisponde a quella della stringa.</span><span class="sxs-lookup"><span data-stu-id="8442d-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="8442d-112">Se l'altezza del controllo non è specificata, l'altezza predefinita è una riga.</span><span class="sxs-lookup"><span data-stu-id="8442d-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="8442d-113">Se l'attributo **WordWrap** è impostato su true e l'altezza del controllo è sufficiente per contenere un'altra riga di testo, il testo viene incapsulato in una riga successiva.</span><span class="sxs-lookup"><span data-stu-id="8442d-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="8442d-114">Il wrapping si verifica solo tra le parole.</span><span class="sxs-lookup"><span data-stu-id="8442d-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="8442d-115">È anche possibile forzare le interruzioni di riga, come descritto in **WordWrap**.</span><span class="sxs-lookup"><span data-stu-id="8442d-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="8442d-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="8442d-116">Examples</span></span>

<span data-ttu-id="8442d-117">L'esempio seguente è un file di definizione dell'interfaccia completa che illustra come vengono usati gli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="8442d-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="8442d-118">Si trova nella directory degli esempi installata con l'SDK.</span><span class="sxs-lookup"><span data-stu-id="8442d-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="8442d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8442d-119">Requirements</span></span>



| <span data-ttu-id="8442d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8442d-120">Requirement</span></span> | <span data-ttu-id="8442d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8442d-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8442d-122">Versione</span><span class="sxs-lookup"><span data-stu-id="8442d-122">Version</span></span><br/> | <span data-ttu-id="8442d-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="8442d-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8442d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8442d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8442d-125">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="8442d-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="8442d-126">**TESTO. toolTip**</span><span class="sxs-lookup"><span data-stu-id="8442d-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="8442d-127">**TESTO. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="8442d-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





