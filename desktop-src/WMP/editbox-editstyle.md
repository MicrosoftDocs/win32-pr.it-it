---
title: CASELLA. editStyle
description: L'attributo editStyle specifica o recupera lo stile del controllo casella di modifica.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- Media Player Windows casella. editStyle
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329936"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="92058-104">CASELLA. editStyle</span><span class="sxs-lookup"><span data-stu-id="92058-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="92058-105">L'attributo **editStyle** specifica o recupera lo stile del controllo casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="92058-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="92058-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="92058-106">Possible Values</span></span>

<span data-ttu-id="92058-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="92058-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="92058-108">Valore</span><span class="sxs-lookup"><span data-stu-id="92058-108">Value</span></span>     | <span data-ttu-id="92058-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92058-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="92058-110">normale</span><span class="sxs-lookup"><span data-stu-id="92058-110">normal</span></span>    | <span data-ttu-id="92058-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="92058-111">Default.</span></span> <span data-ttu-id="92058-112">Visualizza il testo normale su una sola riga.</span><span class="sxs-lookup"><span data-stu-id="92058-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="92058-113">password</span><span class="sxs-lookup"><span data-stu-id="92058-113">password</span></span>  | <span data-ttu-id="92058-114">Visualizza gli asterischi ( \* ) al posto del testo.</span><span class="sxs-lookup"><span data-stu-id="92058-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="92058-115">Può essere specificato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="92058-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="92058-116">maiuscole</span><span class="sxs-lookup"><span data-stu-id="92058-116">uppercase</span></span> | <span data-ttu-id="92058-117">Visualizza il testo come tutti i caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="92058-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="92058-118">lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="92058-118">lowercase</span></span> | <span data-ttu-id="92058-119">Visualizza il testo in caratteri minuscoli.</span><span class="sxs-lookup"><span data-stu-id="92058-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="92058-120">d'acquisto</span><span class="sxs-lookup"><span data-stu-id="92058-120">number</span></span>    | <span data-ttu-id="92058-121">Visualizza solo numeri.</span><span class="sxs-lookup"><span data-stu-id="92058-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="92058-122">Multiline</span><span class="sxs-lookup"><span data-stu-id="92058-122">multiline</span></span> | <span data-ttu-id="92058-123">Visualizza più righe di testo.</span><span class="sxs-lookup"><span data-stu-id="92058-123">Displays multiple lines of text.</span></span> <span data-ttu-id="92058-124">Può essere specificato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="92058-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="92058-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="92058-125">Remarks</span></span>

<span data-ttu-id="92058-126">Questo attributo può essere impostato solo su "password" o "Multiline" in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="92058-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="92058-127">Se è impostato su "Multiline", il valore non può essere modificato in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="92058-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="92058-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92058-128">Requirements</span></span>



| <span data-ttu-id="92058-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="92058-129">Requirement</span></span> | <span data-ttu-id="92058-130">Valore</span><span class="sxs-lookup"><span data-stu-id="92058-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="92058-131">Versione</span><span class="sxs-lookup"><span data-stu-id="92058-131">Version</span></span><br/> | <span data-ttu-id="92058-132">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="92058-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92058-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92058-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92058-134">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="92058-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





