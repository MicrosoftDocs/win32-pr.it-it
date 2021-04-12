---
description: La proprietà ButtonsAvailable Recupera il numero totale di pulsanti nel menu corrente.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Proprietà ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401274"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="9e2cb-103">Proprietà ButtonsAvailable</span><span class="sxs-lookup"><span data-stu-id="9e2cb-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="9e2cb-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9e2cb-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9e2cb-106">La `ButtonsAvailable` proprietà recupera il numero totale di pulsanti nel menu corrente.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="9e2cb-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e2cb-107">Return Value</span></span>

<span data-ttu-id="9e2cb-108">Restituisce un valore intero che rappresenta il numero di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e2cb-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e2cb-109">Remarks</span></span>

<span data-ttu-id="9e2cb-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-110">This property is read-only with no default value.</span></span> <span data-ttu-id="9e2cb-111">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="9e2cb-112">Chiamare questo metodo per recuperare il limite superiore per l'intervallo di numeri di pulsante validi.</span><span class="sxs-lookup"><span data-stu-id="9e2cb-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e2cb-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e2cb-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2cb-114">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="9e2cb-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="9e2cb-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="9e2cb-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="9e2cb-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="9e2cb-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="9e2cb-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="9e2cb-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="9e2cb-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="9e2cb-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



