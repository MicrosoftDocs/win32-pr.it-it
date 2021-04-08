---
description: Il metodo SelectAtPosition seleziona il pulsante di menu in corrispondenza delle coordinate del puntatore del mouse specificate.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Metodo SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746250"
---
# <a name="selectatposition-method"></a><span data-ttu-id="56d62-103">Metodo SelectAtPosition</span><span class="sxs-lookup"><span data-stu-id="56d62-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="56d62-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56d62-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="56d62-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="56d62-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="56d62-106">Il `SelectAtPosition` metodo seleziona il pulsante di menu in corrispondenza delle coordinate del puntatore del mouse specificate.</span><span class="sxs-lookup"><span data-stu-id="56d62-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="56d62-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="56d62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56d62-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="56d62-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="56d62-109">Specifica la coordinata x come intero.</span><span class="sxs-lookup"><span data-stu-id="56d62-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="56d62-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="56d62-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="56d62-111">Specifica la coordinata y come intero.</span><span class="sxs-lookup"><span data-stu-id="56d62-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56d62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56d62-112">Return Value</span></span>

<span data-ttu-id="56d62-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="56d62-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56d62-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="56d62-114">Remarks</span></span>

<span data-ttu-id="56d62-115">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="56d62-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="56d62-116">Se si seleziona semplicemente, il pulsante viene evidenziato.</span><span class="sxs-lookup"><span data-stu-id="56d62-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="56d62-117">Per inviare il comando associato a un pulsante che è stato selezionato, chiamare [**ActivateButton**](activatebutton-method.md).</span><span class="sxs-lookup"><span data-stu-id="56d62-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="56d62-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56d62-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d62-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="56d62-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="56d62-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="56d62-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="56d62-121">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="56d62-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="56d62-122">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="56d62-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="56d62-123">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="56d62-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



