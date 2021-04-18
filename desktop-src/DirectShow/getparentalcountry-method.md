---
description: Il metodo DVDAdm. GetParentalCountry Recupera il paese padre/area che è stato salvato per ultimo nel registro di sistema.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Metodo GetParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330933"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="cbe8f-103">Metodo GetParentalCountry</span><span class="sxs-lookup"><span data-stu-id="cbe8f-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="cbe8f-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cbe8f-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cbe8f-106">Il `DVDAdm.GetParentalCountry` metodo recupera il paese padre/area che è stato salvato per l'ultima volta nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="cbe8f-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbe8f-107">Return Value</span></span>

<span data-ttu-id="cbe8f-108">Restituisce un intero che indica il codice del paese/area geografica predefinito archiviato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbe8f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbe8f-109">Remarks</span></span>

<span data-ttu-id="cbe8f-110">Il paese/area padre recuperato da questo metodo non è necessariamente lo stesso paese/regione attualmente archiviato nell'oggetto MSWebDVD.</span><span class="sxs-lookup"><span data-stu-id="cbe8f-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe8f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbe8f-111">Requirements</span></span>



| <span data-ttu-id="cbe8f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbe8f-112">Requirement</span></span> | <span data-ttu-id="cbe8f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cbe8f-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe8f-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbe8f-114">Header</span></span><br/> | <dl> <span data-ttu-id="cbe8f-115"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe8f-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe8f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbe8f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe8f-117">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="cbe8f-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




