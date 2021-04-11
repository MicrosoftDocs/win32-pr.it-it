---
description: La proprietà CurrentButton Recupera il numero del pulsante di menu selezionato.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Proprietà CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341861"
---
# <a name="currentbutton-property"></a><span data-ttu-id="e29f4-103">Proprietà CurrentButton</span><span class="sxs-lookup"><span data-stu-id="e29f4-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="e29f4-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e29f4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e29f4-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e29f4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e29f4-106">La `CurrentButton` proprietà recupera il numero del pulsante di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="e29f4-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="e29f4-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e29f4-107">Return Value</span></span>

<span data-ttu-id="e29f4-108">Restituisce un valore intero che rappresenta il pulsante.</span><span class="sxs-lookup"><span data-stu-id="e29f4-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="e29f4-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e29f4-109">Remarks</span></span>

<span data-ttu-id="e29f4-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e29f4-110">This property is read-only with no default value.</span></span> <span data-ttu-id="e29f4-111">Utilizzare questo metodo quando si implementa la gestione personalizzata del mouse dopo l'impostazione di [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="e29f4-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e29f4-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e29f4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29f4-113">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="e29f4-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="e29f4-114">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="e29f4-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="e29f4-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="e29f4-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="e29f4-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="e29f4-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="e29f4-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="e29f4-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="e29f4-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="e29f4-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



