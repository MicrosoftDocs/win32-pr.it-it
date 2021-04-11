---
description: Il metodo GetButtonRect Recupera il rettangolo per il pulsante specificato, nelle coordinate della finestra.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Metodo GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123534"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="9707a-103">Metodo GetButtonRect</span><span class="sxs-lookup"><span data-stu-id="9707a-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="9707a-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9707a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9707a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9707a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9707a-106">Il `GetButtonRect` metodo recupera il rettangolo per il pulsante specificato, in coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="9707a-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="9707a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9707a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9707a-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="9707a-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="9707a-109">Specifica il numero di pulsante come intero.</span><span class="sxs-lookup"><span data-stu-id="9707a-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9707a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9707a-110">Return Value</span></span>

<span data-ttu-id="9707a-111">Restituisce un oggetto [DVDRect](dvdrect-object.md) che definisce il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="9707a-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="9707a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9707a-112">Remarks</span></span>

<span data-ttu-id="9707a-113">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="9707a-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9707a-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9707a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9707a-115">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="9707a-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="9707a-116">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="9707a-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="9707a-117">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="9707a-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="9707a-118">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="9707a-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="9707a-119">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="9707a-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



