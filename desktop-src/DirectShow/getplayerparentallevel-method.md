---
description: GetPlayerParentalLevel Recupera il livello di gestione padre impostato nell'oggetto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Metodo GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123498"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="97275-103">Metodo GetPlayerParentalLevel</span><span class="sxs-lookup"><span data-stu-id="97275-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="97275-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="97275-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="97275-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="97275-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="97275-106">`GetPlayerParentalLevel`Recupera il livello di gestione padre impostato nell'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="97275-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="97275-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97275-107">Return Value</span></span>

<span data-ttu-id="97275-108">Restituisce un valore intero che specifica il livello padre corrente nel navigatore DVD oppure-1 se la gestione padre è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="97275-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="97275-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="97275-109">Remarks</span></span>

<span data-ttu-id="97275-110">Un'applicazione lettore è responsabile dell'applicazione dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="97275-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="97275-111">Il livello padre del lettore è un valore impostato da un'applicazione che può essere usato per indicare il livello padre più alto che l'utente corrente può visualizzare.</span><span class="sxs-lookup"><span data-stu-id="97275-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="97275-112">Quando il navigatore DVD rileva un nuovo livello padre, usare questo metodo per determinare se il nuovo livello è maggiore del livello impostato dall'applicazione tramite [**SelectParentalLevel**](selectparentallevel-method.md).</span><span class="sxs-lookup"><span data-stu-id="97275-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="97275-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97275-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97275-114">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="97275-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="97275-115">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="97275-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="97275-116">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="97275-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="97275-117">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="97275-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



