---
title: MONTHDAYSTATE
description: Il tipo di dati MONTHDAYSTATE è un bit che include lo stato di ogni giorno di un mese.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855498"
---
# <a name="monthdaystate"></a><span data-ttu-id="72920-103">MONTHDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="72920-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="72920-104">Il tipo di dati MONTHDAYSTATE è un bit che include lo stato di ogni giorno di un mese.</span><span class="sxs-lookup"><span data-stu-id="72920-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="72920-105">Il tipo di dati è definito in commctrl. h come segue:</span><span class="sxs-lookup"><span data-stu-id="72920-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="72920-106">Ogni bit (da 0 a 30) rappresenta lo stato di un giorno in un mese.</span><span class="sxs-lookup"><span data-stu-id="72920-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="72920-107">Se un bit è acceso, il giorno corrispondente verrà visualizzato in grassetto. in caso contrario, verrà visualizzato senza enfasi.</span><span class="sxs-lookup"><span data-stu-id="72920-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="72920-108">Questo tipo di dati viene usato con il messaggio [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) e con la macro corrispondente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="72920-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="72920-109">Quando i valori di MONTHDAYSTATE vengono utilizzati in riferimento a mesi inferiori a 31 giorni, sarà possibile accedere solo ai bit necessari.</span><span class="sxs-lookup"><span data-stu-id="72920-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="72920-110">Questo tipo di dati è stato definito per la prima volta nella [versione 4,70](common-control-versions.md) del Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="72920-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




