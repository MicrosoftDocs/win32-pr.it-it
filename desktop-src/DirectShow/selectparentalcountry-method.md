---
description: Il metodo SelectParentalCountry imposta il paese/area padre specificato per la riproduzione successiva.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Metodo SelectParentalCountry
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522178"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="ffeb3-103">Metodo SelectParentalCountry</span><span class="sxs-lookup"><span data-stu-id="ffeb3-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="ffeb3-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ffeb3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ffeb3-106">Il `SelectParentalCountry` metodo imposta il paese/area padre specificato per la riproduzione successiva.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="ffeb3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffeb3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffeb3-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="ffeb3-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="ffeb3-109">Specifica il paese/area geografica come intero.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="ffeb3-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="ffeb3-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="ffeb3-111">Specifica l'utente correntemente connesso sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="ffeb3-112">(Attualmente ignorata).</span><span class="sxs-lookup"><span data-stu-id="ffeb3-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="ffeb3-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="ffeb3-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="ffeb3-114">Specifica la stringa della password dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffeb3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffeb3-115">Return Value</span></span>

<span data-ttu-id="ffeb3-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffeb3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffeb3-117">Remarks</span></span>

<span data-ttu-id="ffeb3-118">Il paese/area padre determina come vengono interpretati i livelli padre.</span><span class="sxs-lookup"><span data-stu-id="ffeb3-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffeb3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffeb3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffeb3-120">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="ffeb3-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="ffeb3-121">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="ffeb3-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="ffeb3-122">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="ffeb3-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="ffeb3-123">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="ffeb3-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="ffeb3-124">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="ffeb3-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="ffeb3-125">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="ffeb3-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



