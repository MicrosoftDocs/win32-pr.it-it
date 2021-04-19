---
title: ClosedCaption.SAMILang
description: La proprietà SAMILang specifica o recupera la lingua visualizzata per la didascalia chiusa.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Media Player Windows ClosedCaption. SAMILang
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326730"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="d4847-104">ClosedCaption.SAMILang</span><span class="sxs-lookup"><span data-stu-id="d4847-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="d4847-105">La proprietà **SAMILang** specifica o recupera la lingua visualizzata per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="d4847-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="d4847-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d4847-106">Possible Values</span></span>

<span data-ttu-id="d4847-107">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d4847-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4847-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4847-108">Remarks</span></span>

<span data-ttu-id="d4847-109">Un file SAMI può contenere testo per una o più lingue.</span><span class="sxs-lookup"><span data-stu-id="d4847-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="d4847-110">Le lingue disponibili per la didascalia chiusa sono definite tra i tag <STYLE> e </STYLE> nel file Sami.</span><span class="sxs-lookup"><span data-stu-id="d4847-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="d4847-111">Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="d4847-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="d4847-112">Il nome specificato per una lingua può essere qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="d4847-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="d4847-113">È ad esempio possibile utilizzare il codice seguente per definire l'inglese (Stati Uniti):</span><span class="sxs-lookup"><span data-stu-id="d4847-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="d4847-114">Se non si specifica alcun linguaggio SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="d4847-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="d4847-115">Valore passato utilizzando *ClosedCaption*. **SAMILang** deve corrispondere all'attributo **Name** nell'identificatore di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="d4847-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="d4847-116">**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="d4847-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="d4847-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="d4847-117">Examples</span></span>

<span data-ttu-id="d4847-118">Nell'esempio JScript seguente viene usato *ClosedCaption*. **SAMILang** in un elemento HTML SELECT per specificare la lingua del titolo closed.</span><span class="sxs-lookup"><span data-stu-id="d4847-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="d4847-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d4847-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="d4847-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4847-120">Requirements</span></span>



| <span data-ttu-id="d4847-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4847-121">Requirement</span></span> | <span data-ttu-id="d4847-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d4847-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4847-123">Versione</span><span class="sxs-lookup"><span data-stu-id="d4847-123">Version</span></span><br/> | <span data-ttu-id="d4847-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="d4847-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4847-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d4847-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4847-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4847-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4847-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4847-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4847-128">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="d4847-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="d4847-129">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="d4847-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





