---
description: I dispositivi portatili Windows supportano le proprietà di appuntamento seguenti.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Proprietà appuntamento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331829"
---
# <a name="appointment-properties"></a><span data-ttu-id="e3986-103">Proprietà appuntamento</span><span class="sxs-lookup"><span data-stu-id="e3986-103">Appointment Properties</span></span>

<span data-ttu-id="e3986-104">I dispositivi portatili Windows supportano le proprietà di appuntamento seguenti.</span><span class="sxs-lookup"><span data-stu-id="e3986-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="e3986-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3986-105">Property</span></span>                                   | <span data-ttu-id="e3986-106">VarType</span><span class="sxs-lookup"><span data-stu-id="e3986-106">VarType</span></span>        | <span data-ttu-id="e3986-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3986-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e3986-108">**\_ \_ partecipanti accettati appuntamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e3986-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="e3986-109">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-110">Elenco delimitato da punti e virgola dei partecipanti che hanno accettato l'appuntamento.</span><span class="sxs-lookup"><span data-stu-id="e3986-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="e3986-111">**WPD \_ appuntamento \_ rifiutato \_**</span><span class="sxs-lookup"><span data-stu-id="e3986-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="e3986-112">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-113">Elenco delimitato da punti e virgola di partecipanti che hanno rifiutato l'appuntamento.</span><span class="sxs-lookup"><span data-stu-id="e3986-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="e3986-114">**\_località appuntamento \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e3986-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="e3986-115">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="e3986-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="e3986-116">Posizione descrittiva dell'appuntamento, ad esempio, "Building 5, Room 7".</span><span class="sxs-lookup"><span data-stu-id="e3986-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="e3986-117">**\_ \_ partecipanti facoltativi appuntamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e3986-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="e3986-118">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-119">Elenco delimitato da punti e virgola di partecipanti facoltativi per l'appuntamento.</span><span class="sxs-lookup"><span data-stu-id="e3986-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="e3986-120">**\_ \_ partecipanti richiesti per l'appuntamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e3986-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="e3986-121">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-122">Elenco delimitato da punti e virgola dei partecipanti richiesti per l'appuntamento.</span><span class="sxs-lookup"><span data-stu-id="e3986-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="e3986-123">**\_risorse appuntamento \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e3986-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="e3986-124">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-125">Elenco delimitato da punti e virgola delle risorse necessarie per l'appuntamento.</span><span class="sxs-lookup"><span data-stu-id="e3986-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="e3986-126">**\_ \_ partecipanti provvisorio di appuntamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e3986-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="e3986-127">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-128">Elenco delimitato da punti e virgola dei partecipanti che hanno accettato provvisoriamente l'appuntamento.</span><span class="sxs-lookup"><span data-stu-id="e3986-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="e3986-129">**\_tipo di appuntamento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e3986-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="e3986-130">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e3986-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e3986-131">Tipo di appuntamento, ad esempio, "personale", "business" e così via.</span><span class="sxs-lookup"><span data-stu-id="e3986-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="e3986-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3986-132">Requirements</span></span>



| <span data-ttu-id="e3986-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3986-133">Requirement</span></span> | <span data-ttu-id="e3986-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e3986-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3986-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3986-135">Header</span></span><br/> | <dl> <span data-ttu-id="e3986-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3986-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3986-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3986-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3986-138">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="e3986-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




