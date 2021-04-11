---
description: Il metodo GetButtonAtPosition Recupera il numero del pulsante in corrispondenza delle coordinate specificate senza selezionarlo o attivarlo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Metodo GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123537"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="8d093-103">Metodo GetButtonAtPosition</span><span class="sxs-lookup"><span data-stu-id="8d093-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="8d093-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8d093-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8d093-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="8d093-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8d093-106">Il `GetButtonAtPosition` metodo recupera il numero del pulsante in corrispondenza delle coordinate specificate senza selezionarlo o attivarlo.</span><span class="sxs-lookup"><span data-stu-id="8d093-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="8d093-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d093-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d093-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="8d093-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="8d093-109">Specifica la coordinata x del puntatore del mouse come intero.</span><span class="sxs-lookup"><span data-stu-id="8d093-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8d093-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="8d093-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="8d093-111">Specifica la coordinata y del puntatore del mouse come intero.</span><span class="sxs-lookup"><span data-stu-id="8d093-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d093-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d093-112">Return Value</span></span>

<span data-ttu-id="8d093-113">Restituisce un valore intero che specifica il pulsante, se presente, in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="8d093-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d093-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d093-114">Remarks</span></span>

<span data-ttu-id="8d093-115">Questo metodo restituisce zero se non è presente alcun pulsante in corrispondenza delle coordinate specificate.</span><span class="sxs-lookup"><span data-stu-id="8d093-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="8d093-116">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="8d093-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d093-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d093-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d093-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="8d093-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="8d093-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="8d093-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="8d093-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="8d093-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="8d093-121">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="8d093-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="8d093-122">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="8d093-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="8d093-123">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="8d093-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



