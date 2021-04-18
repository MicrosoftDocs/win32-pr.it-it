---
description: Il metodo AcceptParentalLevelChange accetta o rifiuta il nuovo livello di gestione padre temporaneo.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Metodo AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304276"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="f4e8c-103">Metodo AcceptParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="f4e8c-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="f4e8c-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f4e8c-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f4e8c-106">Il metodo AcceptParentalLevelChange accetta o rifiuta il nuovo livello di gestione padre temporaneo.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="f4e8c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4e8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e8c-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span><span class="sxs-lookup"><span data-stu-id="f4e8c-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="f4e8c-109">Specifica il nuovo livello padre come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="f4e8c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f4e8c-110">Value</span></span> | <span data-ttu-id="f4e8c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4e8c-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="f4e8c-112">true</span><span class="sxs-lookup"><span data-stu-id="f4e8c-112">true</span></span>  | <span data-ttu-id="f4e8c-113">Accettare il nuovo livello di gestione padre.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="f4e8c-114">false</span><span class="sxs-lookup"><span data-stu-id="f4e8c-114">false</span></span> | <span data-ttu-id="f4e8c-115">Rifiutare il nuovo livello di gestione padre.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e8c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4e8c-116">Return Value</span></span>

<span data-ttu-id="f4e8c-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e8c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4e8c-118">Remarks</span></span>

<span data-ttu-id="f4e8c-119">Chiamare questo metodo in risposta a una \_ notifica degli \_ eventi di modifica del livello padre di un DVD EC \_ \_ per specificare se il navigatore DVD deve riprodurre il contenuto con il nuovo livello padre oppure creare un ramo in cui il disco specifichi se il nuovo livello viene rifiutato.</span><span class="sxs-lookup"><span data-stu-id="f4e8c-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4e8c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4e8c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e8c-121">Applicazione dei livelli di gestione padre</span><span class="sxs-lookup"><span data-stu-id="f4e8c-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="f4e8c-122">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="f4e8c-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="f4e8c-123">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="f4e8c-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="f4e8c-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="f4e8c-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="f4e8c-125">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="f4e8c-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="f4e8c-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="f4e8c-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="f4e8c-127">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="f4e8c-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



