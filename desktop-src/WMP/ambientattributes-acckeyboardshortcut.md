---
title: AmbientAttributes. accKeyboardShortcut
description: L'attributo accKeyboardShortcut specifica o Recupera una descrizione del tasto di scelta rapida per qualsiasi elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- Media Player Windows AmbientAttributes. accKeyboardShortcut
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326742"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="10ba8-104">AmbientAttributes. accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="10ba8-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="10ba8-105">L'attributo **accKeyboardShortcut** specifica o Recupera una descrizione del tasto di scelta rapida per qualsiasi elemento.</span><span class="sxs-lookup"><span data-stu-id="10ba8-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="10ba8-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="10ba8-106">Possible Values</span></span>

<span data-ttu-id="10ba8-107">Questo attributo è una **stringa** di lettura/scrittura con un valore predefinito di "" (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="10ba8-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="10ba8-108">Per l'elemento **Button** , il valore predefinito di questo attributo è "barra spaziatrice o invio".</span><span class="sxs-lookup"><span data-stu-id="10ba8-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="10ba8-109">Per l'elemento **Slider** , il valore predefinito è "freccia destra/freccia su per aumentare, freccia sinistra/giù per diminuire".</span><span class="sxs-lookup"><span data-stu-id="10ba8-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="10ba8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="10ba8-110">Remarks</span></span>

<span data-ttu-id="10ba8-111">Questo attributo viene utilizzato per scopi di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="10ba8-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="10ba8-112">Consente una descrizione del tasto di scelta rapida per qualsiasi elemento da leggere ad alta voce da un programma Reader.</span><span class="sxs-lookup"><span data-stu-id="10ba8-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="10ba8-113">Questo attributo non imposta il collegamento.</span><span class="sxs-lookup"><span data-stu-id="10ba8-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="10ba8-114">Lo Scripter deve eseguire tale operazione.</span><span class="sxs-lookup"><span data-stu-id="10ba8-114">The scripter must do that work.</span></span>

<span data-ttu-id="10ba8-115">Questo attributo si applica anche agli elementi Button all'interno del controllo gruppo di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="10ba8-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ba8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10ba8-116">Requirements</span></span>



| <span data-ttu-id="10ba8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ba8-117">Requirement</span></span> | <span data-ttu-id="10ba8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="10ba8-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="10ba8-119">Versione</span><span class="sxs-lookup"><span data-stu-id="10ba8-119">Version</span></span><br/> | <span data-ttu-id="10ba8-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="10ba8-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10ba8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10ba8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ba8-122">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="10ba8-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





