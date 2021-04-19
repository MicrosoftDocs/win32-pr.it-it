---
description: L'evento DVDNotify notifica a un'applicazione di molti eventi DVD e istruzioni per i dischi diversi.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329262"
---
# <a name="dvdnotify"></a><span data-ttu-id="9c9b6-103">DVDNotify</span><span class="sxs-lookup"><span data-stu-id="9c9b6-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="9c9b6-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c9b6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9c9b6-106">L' `DVDNotify` evento invia una notifica all'applicazione di molti eventi DVD e istruzioni per i dischi diversi.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="9c9b6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c9b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c9b6-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="9c9b6-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="9c9b6-109">Specifica il codice di notifica dell'evento DVD.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9c9b6-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span><span class="sxs-lookup"><span data-stu-id="9c9b6-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="9c9b6-111">Può contenere informazioni aggiuntive correlate all'evento.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="9c9b6-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="9c9b6-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="9c9b6-113">Può contenere informazioni aggiuntive correlate all'evento.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c9b6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c9b6-114">Remarks</span></span>

<span data-ttu-id="9c9b6-115">I [codici di notifica degli eventi DVD](dvd-notification-codes.md) forniscono una spiegazione completa di tutti i codici di notifica degli eventi DVD e dei relativi parametri.</span><span class="sxs-lookup"><span data-stu-id="9c9b6-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c9b6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c9b6-116">Requirements</span></span>



| <span data-ttu-id="9c9b6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c9b6-117">Requirement</span></span> | <span data-ttu-id="9c9b6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9c9b6-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9b6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c9b6-119">Header</span></span><br/> | <dl> <span data-ttu-id="9c9b6-120"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c9b6-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




