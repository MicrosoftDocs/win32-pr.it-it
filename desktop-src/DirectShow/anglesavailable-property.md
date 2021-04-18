---
description: La proprietà AnglesAvailable Recupera il numero di angoli attualmente disponibili.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Proprietà AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304152"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="649df-103">Proprietà AnglesAvailable</span><span class="sxs-lookup"><span data-stu-id="649df-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="649df-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="649df-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="649df-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="649df-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="649df-106">La `AnglesAvailable` proprietà recupera il numero di angoli attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="649df-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="649df-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="649df-107">Return Value</span></span>

<span data-ttu-id="649df-108">Restituisce un valore intero compreso tra 1 e 9 che rappresenta il numero di angoli attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="649df-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="649df-109">Se</span><span class="sxs-lookup"><span data-stu-id="649df-109">If</span></span>


```
iAngles
```



<span data-ttu-id="649df-110">= 1, nessun blocco angolo nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="649df-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="649df-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="649df-111">Remarks</span></span>

<span data-ttu-id="649df-112">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="649df-112">This property is read-only with no default value.</span></span> <span data-ttu-id="649df-113">Un *blocco Angle* è un segmento video che è stato ripreso da più di un angolo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="649df-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="649df-114">In un blocco angolo possono essere presenti fino a nove angoli, numerati da 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="649df-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="649df-115">Quando il navigatore DVD passa per la prima volta a un blocco angolo, invia all'applicazione una \_ \_ \_ notifica degli eventi disponibili per gli angoli di DVD EC con il numero di angoli in *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="649df-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="649df-116">È possibile creare un disco per visualizzare automaticamente un menu per gli angoli disponibili quando entra in un blocco angolo, ma in genere un'applicazione deve determinare il numero di angoli disponibili e fornire all'utente un modo per selezionarne uno.</span><span class="sxs-lookup"><span data-stu-id="649df-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="649df-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="649df-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649df-118">**CurrentAngle**</span><span class="sxs-lookup"><span data-stu-id="649df-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



