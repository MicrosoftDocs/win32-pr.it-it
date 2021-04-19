---
title: TESTO. wordWrap
description: L'attributo wordWrap specifica o recupera un valore che indica se il ritorno a capo automatico è abilitato o disabilitato.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Media Player di Windows TEXT. wordWrap
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331849"
---
# <a name="textwordwrap"></a><span data-ttu-id="4700d-104">TESTO. wordWrap</span><span class="sxs-lookup"><span data-stu-id="4700d-104">TEXT.wordWrap</span></span>

<span data-ttu-id="4700d-105">L'attributo **WordWrap** specifica o recupera un valore che indica se il ritorno a capo automatico è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4700d-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="4700d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="4700d-106">Possible Values</span></span>

<span data-ttu-id="4700d-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4700d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="4700d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4700d-108">Value</span></span> | <span data-ttu-id="4700d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4700d-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4700d-110">true</span><span class="sxs-lookup"><span data-stu-id="4700d-110">true</span></span>  | <span data-ttu-id="4700d-111">Ritorno a capo automatico abilitato.</span><span class="sxs-lookup"><span data-stu-id="4700d-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="4700d-112">false</span><span class="sxs-lookup"><span data-stu-id="4700d-112">false</span></span> | <span data-ttu-id="4700d-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4700d-113">Default.</span></span> <span data-ttu-id="4700d-114">Ritorno a capo automatico disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4700d-114">Word wrap is disabled.</span></span> <span data-ttu-id="4700d-115">Se il testo non rientra nel controllo, il testo viene ritagliato.</span><span class="sxs-lookup"><span data-stu-id="4700d-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4700d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4700d-116">Remarks</span></span>

<span data-ttu-id="4700d-117">Il controllo testo non divide le parole.</span><span class="sxs-lookup"><span data-stu-id="4700d-117">The Text control does not split words apart.</span></span> <span data-ttu-id="4700d-118">Se una parola si estende oltre la larghezza del controllo, viene utilizzato il ritorno a capo automatico per spostare la parola nella riga successiva.</span><span class="sxs-lookup"><span data-stu-id="4700d-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="4700d-119">Se una singola parola supera la larghezza del controllo, tale parola viene ritagliata e occupa una sola riga.</span><span class="sxs-lookup"><span data-stu-id="4700d-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="4700d-120">Se l'attributo **Width** non è specificato, **WordWrap** viene ignorato e il controllo di testo verrà ridimensionato anziché racchiudere il testo.</span><span class="sxs-lookup"><span data-stu-id="4700d-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="4700d-121">Se si desiderano interruzioni di riga in posizioni particolari, è necessario specificare in modo esplicito il **valore** utilizzando "&\# 13;" o " \\ r".</span><span class="sxs-lookup"><span data-stu-id="4700d-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="4700d-122">Se il secondo formato viene usato quando si specifica direttamente il valore, la stringa deve essere preceduta da "JScript:" e il valore effettivo deve essere racchiuso tra virgolette singole, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4700d-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="4700d-123">Questa operazione non è necessaria se il valore viene impostato dinamicamente dall'interno di un gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="4700d-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="4700d-124">Se **WordWrap** è impostato su true e la **Descrizione comando** non è specificata, la descrizione comando visualizzerà il testo completo dell'attributo **value** .</span><span class="sxs-lookup"><span data-stu-id="4700d-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="4700d-125">Se non si desidera alcuna descrizione comando, impostare **ToolTip** su "" (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="4700d-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="4700d-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="4700d-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="4700d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4700d-127">Requirements</span></span>



| <span data-ttu-id="4700d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4700d-128">Requirement</span></span> | <span data-ttu-id="4700d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4700d-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4700d-130">Versione</span><span class="sxs-lookup"><span data-stu-id="4700d-130">Version</span></span><br/> | <span data-ttu-id="4700d-131">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="4700d-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4700d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4700d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4700d-133">**AmbientAttributes. Width**</span><span class="sxs-lookup"><span data-stu-id="4700d-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="4700d-134">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="4700d-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="4700d-135">**TESTO. toolTip**</span><span class="sxs-lookup"><span data-stu-id="4700d-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="4700d-136">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="4700d-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





