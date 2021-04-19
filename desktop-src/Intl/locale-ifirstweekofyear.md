---
description: impostazioni locali \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320219"
---
# <a name="locale_ifirstweekofyear"></a><span data-ttu-id="ec20f-103">impostazioni locali \_ IFIRSTWEEKOFYEAR</span><span class="sxs-lookup"><span data-stu-id="ec20f-103">LOCALE\_IFIRSTWEEKOFYEAR</span></span>

<span data-ttu-id="ec20f-104">Prima settimana dell'anno.</span><span class="sxs-lookup"><span data-stu-id="ec20f-104">The first week of the year.</span></span>



| <span data-ttu-id="ec20f-105">Valore</span><span class="sxs-lookup"><span data-stu-id="ec20f-105">Value</span></span> | <span data-ttu-id="ec20f-106">Significato</span><span class="sxs-lookup"><span data-stu-id="ec20f-106">Meaning</span></span>                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec20f-107">0</span><span class="sxs-lookup"><span data-stu-id="ec20f-107">0</span></span>     | <span data-ttu-id="ec20f-108">La settimana che contiene la 1/1 è la prima settimana dell'anno.</span><span class="sxs-lookup"><span data-stu-id="ec20f-108">Week containing 1/1 is the first week of the year.</span></span> <span data-ttu-id="ec20f-109">Si noti che può essere un singolo giorno, se 1/1 rientra nell'ultimo giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="ec20f-109">Note that this can be a single day, if 1/1 falls on the last day of the week.</span></span> |
| <span data-ttu-id="ec20f-110">1</span><span class="sxs-lookup"><span data-stu-id="ec20f-110">1</span></span>     | <span data-ttu-id="ec20f-111">La prima settimana completa successiva alla 1/1 è la prima settimana dell'anno.</span><span class="sxs-lookup"><span data-stu-id="ec20f-111">First full week following 1/1 is the first week of the year.</span></span>                                                                     |
| <span data-ttu-id="ec20f-112">2</span><span class="sxs-lookup"><span data-stu-id="ec20f-112">2</span></span>     | <span data-ttu-id="ec20f-113">La prima settimana che contiene almeno quattro giorni è la prima settimana dell'anno.</span><span class="sxs-lookup"><span data-stu-id="ec20f-113">First week containing at least four days is the first week of the year.</span></span> <span data-ttu-id="ec20f-114">Compatibile con ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ec20f-114">ISO 8601 compatible.</span></span>                                     |

<span data-ttu-id="ec20f-115">Se LOCALE_IFIRSTWEEKOFYEAR è 2, LOCALE_IFIRSTDAYOFWEEK è 0 (lunedì) e LOCALE_ICALENDARTYPE è gregoriano, la prima settimana segue la definizione ISO 8601 dove la prima settimana è la settimana con il primo giovedì dell'anno gregoriano.</span><span class="sxs-lookup"><span data-stu-id="ec20f-115">If LOCALE_IFIRSTWEEKOFYEAR is 2, LOCALE_IFIRSTDAYOFWEEK is 0 (Monday), and LOCALE_ICALENDARTYPE is Gregorian, then the first week follows the ISO 8601 definition where the first week is the week with the first Thursday of the Gregorian year in it.</span></span>


 

 

 



