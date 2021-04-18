---
title: Stili del controllo calendario mensile (CommCtrl. h)
description: Le costanti di stile seguenti vengono usate durante la creazione di controlli calendario mensile.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327232"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="7837b-103">Stili del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="7837b-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="7837b-104">Le costanti di stile seguenti vengono usate durante la creazione di controlli calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="7837b-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="7837b-105">Costante</span><span class="sxs-lookup"><span data-stu-id="7837b-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="7837b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7837b-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="7837b-107"><dt>**\_DAYSTATE MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="7837b-108">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7837b-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="7837b-109">Il calendario mensile Invia [notifiche \_ GETDAYSTATE di MCN](mcn-getdaystate.md) per richiedere informazioni sui giorni da visualizzare in grassetto.</span><span class="sxs-lookup"><span data-stu-id="7837b-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="7837b-110"><dt>**MultiSelect MCS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="7837b-111">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7837b-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="7837b-112">Il calendario mensile consente all'utente di selezionare un intervallo di date all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="7837b-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="7837b-113">Per impostazione predefinita, l'intervallo massimo è di una settimana.</span><span class="sxs-lookup"><span data-stu-id="7837b-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="7837b-114">È possibile modificare l'intervallo massimo che è possibile selezionare usando il messaggio [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="7837b-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="7837b-115"><dt>**\_su WEEKNUMBERS MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="7837b-116">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7837b-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="7837b-117">Il controllo calendario mensile Visualizza i numeri di settimana (1-52) a sinistra di ogni riga di giorni.</span><span class="sxs-lookup"><span data-stu-id="7837b-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="7837b-118">La settimana 1 è definita come prima settimana che contiene almeno quattro giorni.</span><span class="sxs-lookup"><span data-stu-id="7837b-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="7837b-119"><dt>**\_NOTODAYCIRCLE MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="7837b-120">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7837b-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="7837b-121">Il controllo calendario mensile non esegue il cerchio della data odierna.</span><span class="sxs-lookup"><span data-stu-id="7837b-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="7837b-122"><dt>**MCS \_ NOtoday**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="7837b-123">[Versione 4,70](common-control-versions.md). Il controllo calendario mensile non Visualizza la data "Today" nella parte inferiore del controllo.</span><span class="sxs-lookup"><span data-stu-id="7837b-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="7837b-124"><dt>**\_NOTRAILINGDATES MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="7837b-125">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="7837b-125">**Windows Vista.**</span></span> <span data-ttu-id="7837b-126">Le date dei mesi precedenti e successivi non vengono visualizzate nel calendario del mese corrente.</span><span class="sxs-lookup"><span data-stu-id="7837b-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="7837b-127"><dt>**\_SHORTDAYSOFWEEK MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="7837b-128">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="7837b-128">**Windows Vista.**</span></span> <span data-ttu-id="7837b-129">I nomi dei giorni brevi vengono visualizzati nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="7837b-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="7837b-130"><dt>**\_NOSELCHANGEONNAV MCS**</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="7837b-131">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="7837b-131">**Windows Vista.**</span></span> <span data-ttu-id="7837b-132">La selezione non viene modificata quando l'utente passa a avanti o indietro nel calendario.</span><span class="sxs-lookup"><span data-stu-id="7837b-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="7837b-133">Ciò consente all'utente di selezionare un intervallo maggiore di quello visibile.</span><span class="sxs-lookup"><span data-stu-id="7837b-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="7837b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7837b-134">Requirements</span></span>



| <span data-ttu-id="7837b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7837b-135">Requirement</span></span> | <span data-ttu-id="7837b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7837b-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7837b-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7837b-137">Header</span></span><br/> | <dl> <span data-ttu-id="7837b-138"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7837b-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





