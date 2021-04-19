---
description: Il metodo NotifyParentalLevelChange Abilita o Disabilita la gestione degli eventi per i comandi temporanei del livello di gestione padre.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Metodo NotifyParentalLevelChange (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328073"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="4eb82-103">Metodo NotifyParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="4eb82-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="4eb82-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4eb82-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4eb82-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="4eb82-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4eb82-106">Il `NotifyParentalLevelChange` Metodo Abilita o Disabilita la gestione degli eventi per i comandi temporanei del livello di gestione padre.</span><span class="sxs-lookup"><span data-stu-id="4eb82-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="4eb82-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4eb82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb82-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span><span class="sxs-lookup"><span data-stu-id="4eb82-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="4eb82-109">Specifica un valore booleano che indica se l'applicazione riceve una notifica quando l'oggetto MSWebDVD rileva segmenti video con una classificazione più restrittiva rispetto alla valutazione complessiva del disco.</span><span class="sxs-lookup"><span data-stu-id="4eb82-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb82-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4eb82-110">Return Value</span></span>

<span data-ttu-id="4eb82-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="4eb82-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb82-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4eb82-112">Remarks</span></span>

<span data-ttu-id="4eb82-113">Le notifiche di gestione padre sono disabilitate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4eb82-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="4eb82-114">Ciò significa che i comandi padre temporanei dal disco sono consentiti, ma ignorati e il disco verrà riprodotto senza interruzioni.</span><span class="sxs-lookup"><span data-stu-id="4eb82-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="4eb82-115">Chiamare questo metodo durante l'inizializzazione dell'applicazione se è necessario gestire i comandi temporanei del livello di gestione padre dal disco. Per disabilitare la gestione padre dopo l'abilitazione, chiamare questo metodo con un argomento di false.</span><span class="sxs-lookup"><span data-stu-id="4eb82-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="4eb82-116">Per ulteriori informazioni sulla gestione parentale, vedere [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="4eb82-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb82-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4eb82-117">Requirements</span></span>



| <span data-ttu-id="4eb82-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb82-118">Requirement</span></span> | <span data-ttu-id="4eb82-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4eb82-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb82-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4eb82-120">Header</span></span><br/> | <dl> <span data-ttu-id="4eb82-121"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb82-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb82-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eb82-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb82-123">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="4eb82-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="4eb82-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="4eb82-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="4eb82-125">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="4eb82-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="4eb82-126">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="4eb82-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="4eb82-127">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="4eb82-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




