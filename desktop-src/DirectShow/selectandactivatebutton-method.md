---
description: Il metodo SelectAndActivateButton seleziona e attiva il pulsante specificato.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Metodo SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303876"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="49fee-103">Metodo SelectAndActivateButton</span><span class="sxs-lookup"><span data-stu-id="49fee-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="49fee-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="49fee-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="49fee-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="49fee-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="49fee-106">Il `SelectAndActivateButton` metodo seleziona e attiva il pulsante specificato.</span><span class="sxs-lookup"><span data-stu-id="49fee-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="49fee-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49fee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49fee-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="49fee-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="49fee-109">Specifica il pulsante come intero.</span><span class="sxs-lookup"><span data-stu-id="49fee-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49fee-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49fee-110">Return Value</span></span>

<span data-ttu-id="49fee-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="49fee-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49fee-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="49fee-112">Remarks</span></span>

<span data-ttu-id="49fee-113">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="49fee-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="49fee-114">Questo metodo evidenzia il pulsante specificato e lo attiva automaticamente.</span><span class="sxs-lookup"><span data-stu-id="49fee-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="49fee-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49fee-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fee-116">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="49fee-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="49fee-117">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="49fee-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="49fee-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="49fee-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="49fee-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="49fee-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="49fee-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="49fee-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="49fee-121">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="49fee-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



