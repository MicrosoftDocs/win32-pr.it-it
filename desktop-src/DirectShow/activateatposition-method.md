---
description: Il metodo ActivateAtPosition attiva il pulsante di menu in corrispondenza della posizione specificata.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Metodo ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125328"
---
# <a name="activateatposition-method"></a><span data-ttu-id="a58f9-103">Metodo ActivateAtPosition</span><span class="sxs-lookup"><span data-stu-id="a58f9-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="a58f9-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a58f9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a58f9-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a58f9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a58f9-106">Il metodo ActivateAtPosition attiva il pulsante di menu in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a58f9-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="a58f9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a58f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a58f9-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="a58f9-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="a58f9-109">Specifica la coordinata x come intero.</span><span class="sxs-lookup"><span data-stu-id="a58f9-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="a58f9-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="a58f9-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="a58f9-111">Specifica la coordinata y come intero.</span><span class="sxs-lookup"><span data-stu-id="a58f9-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a58f9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a58f9-112">Return Value</span></span>

<span data-ttu-id="a58f9-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a58f9-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a58f9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a58f9-114">Remarks</span></span>

<span data-ttu-id="a58f9-115">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="a58f9-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a58f9-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a58f9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58f9-117">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="a58f9-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="a58f9-118">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="a58f9-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="a58f9-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="a58f9-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="a58f9-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="a58f9-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="a58f9-121">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="a58f9-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="a58f9-122">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="a58f9-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



