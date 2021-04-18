---
description: Il metodo DVDTimeCode2bstr recupera una stringa che indica l'ora corrente del disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Metodo DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304010"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="7b68b-103">Metodo DVDTimeCode2bstr</span><span class="sxs-lookup"><span data-stu-id="7b68b-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="7b68b-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7b68b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7b68b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="7b68b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7b68b-106">Il `DVDTimeCode2bstr` metodo recupera una stringa che indica l'ora corrente sul disco.</span><span class="sxs-lookup"><span data-stu-id="7b68b-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="7b68b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b68b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b68b-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span><span class="sxs-lookup"><span data-stu-id="7b68b-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="7b68b-109">Specifica l'ora corrente del disco rispetto all'inizio del titolo come numero ottenuto tramite l'evento di [**\_ \_ \_ \_ ora HMSF corrente del DVD EC**](ec-dvd-current-hmsf-time.md) .</span><span class="sxs-lookup"><span data-stu-id="7b68b-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b68b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b68b-110">Return Value</span></span>

<span data-ttu-id="7b68b-111">Restituisce una stringa di 11 caratteri nel formato "HH: mm: SS: FF" che rappresenta le ore, i minuti, i secondi e i frame che definiscono l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="7b68b-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b68b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b68b-112">Remarks</span></span>

<span data-ttu-id="7b68b-113">Questo metodo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7b68b-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b68b-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b68b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b68b-115">Gestione delle notifiche degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="7b68b-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



