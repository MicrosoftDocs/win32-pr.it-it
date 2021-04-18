---
description: Il metodo SelectParentalLevel imposta il livello padre specificato per la riproduzione successiva.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Metodo SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521273"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="9c8b5-103">Metodo SelectParentalLevel</span><span class="sxs-lookup"><span data-stu-id="9c8b5-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="9c8b5-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c8b5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9c8b5-106">Il `SelectParentalLevel` metodo imposta il livello padre specificato per la riproduzione successiva.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="9c8b5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c8b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c8b5-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="9c8b5-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="9c8b5-109">Specifica il livello di gestione padre come intero.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="9c8b5-110">Per abilitare la gestione padre, il parametro *iLevel* deve essere compreso tra 1 e 8.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="9c8b5-111">Per disabilitare la gestione padre, impostare *iLevel* su-1.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="9c8b5-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="9c8b5-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="9c8b5-113">Specifica l'utente corrente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-113">Specifies the current user as a String.</span></span> <span data-ttu-id="9c8b5-114">(Attualmente ignorata).</span><span class="sxs-lookup"><span data-stu-id="9c8b5-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="9c8b5-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="9c8b5-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="9c8b5-116">Specifica la password attualmente archiviata nel registro di sistema sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c8b5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c8b5-117">Return Value</span></span>

<span data-ttu-id="9c8b5-118">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c8b5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c8b5-119">Remarks</span></span>

<span data-ttu-id="9c8b5-120">Questo metodo imposta il livello di accesso nell'oggetto MSWebDVD, che determina il contenuto di cui l'utente può eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="9c8b5-121">I livelli superiori possono riprodurre contenuto di livello inferiore, ma i livelli inferiori non possono riprodurre contenuto di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="9c8b5-122">Il significato esatto dei livelli di gestione padre di otto DVD varia a seconda del paese.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="9c8b5-123">In Stati Uniti e in Canada, viene eseguito il mapping dei livelli alle categorie di classificazione di Motion Picture Association of America (MPAA).</span><span class="sxs-lookup"><span data-stu-id="9c8b5-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="9c8b5-124">Per impostazione predefinita, la gestione padre in DVD Navigator è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="9c8b5-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c8b5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c8b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c8b5-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="9c8b5-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="9c8b5-127">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="9c8b5-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="9c8b5-128">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="9c8b5-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="9c8b5-129">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="9c8b5-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="9c8b5-130">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="9c8b5-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="9c8b5-131">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="9c8b5-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



