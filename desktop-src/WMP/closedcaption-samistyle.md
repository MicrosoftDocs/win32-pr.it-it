---
title: ClosedCaption.SAMIStyle
description: La proprietà SAMIStyle specifica o recupera lo stile dei sottotitoli codificati.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- Media Player Windows ClosedCaption. SAMIStyle
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326728"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="2b6c8-104">ClosedCaption.SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="2b6c8-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="2b6c8-105">La proprietà **SAMIStyle** specifica o recupera lo stile dei sottotitoli codificati.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="2b6c8-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="2b6c8-106">Possible Values</span></span>

<span data-ttu-id="2b6c8-107">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6c8-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b6c8-108">Remarks</span></span>

<span data-ttu-id="2b6c8-109">Un file SAMI può contenere diverse definizioni di stile del formato.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="2b6c8-110">Gli stili SAMI sono definiti tra i tag <STYLE> e </STYLE> nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="2b6c8-111">Uno stile viene definito con una stringa di testo preceduta da un \# carattere.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="2b6c8-112">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2b6c8-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="2b6c8-113">Specifica uno stile che produce un tipo di carattere specifico.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="2b6c8-114">Se non viene specificato alcuno stile SAMI, per impostazione predefinita viene usato il primo stile definito nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="2b6c8-115">**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="2b6c8-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="2b6c8-116">Examples</span></span>

<span data-ttu-id="2b6c8-117">Nell'esempio JScript seguente viene creato un elemento HTML SELECT che usa *closedCaption*. **SAMIStyle** per modificare l'aspetto del testo della didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="2b6c8-118">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2b6c8-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="2b6c8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b6c8-119">Requirements</span></span>



| <span data-ttu-id="2b6c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b6c8-120">Requirement</span></span> | <span data-ttu-id="2b6c8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2b6c8-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6c8-122">Versione</span><span class="sxs-lookup"><span data-stu-id="2b6c8-122">Version</span></span><br/> | <span data-ttu-id="2b6c8-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="2b6c8-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2b6c8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6c8-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2b6c8-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b6c8-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6c8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b6c8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6c8-127">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="2b6c8-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="2b6c8-128">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="2b6c8-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





