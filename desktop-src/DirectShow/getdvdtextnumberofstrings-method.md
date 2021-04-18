---
description: Il metodo GetDVDTextNumberOfStrings Recupera il numero di stringhe di testo disponibili per la lingua specificata.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Metodo GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304198"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="96106-103">Metodo GetDVDTextNumberOfStrings</span><span class="sxs-lookup"><span data-stu-id="96106-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="96106-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="96106-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="96106-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="96106-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="96106-106">Il `GetDVDTextNumberOfStrings` metodo recupera il numero di stringhe di testo disponibili per la lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="96106-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="96106-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="96106-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96106-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="96106-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="96106-109">Specifica il linguaggio come intero.</span><span class="sxs-lookup"><span data-stu-id="96106-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="96106-110">Il valore deve essere compreso tra zero e uno minore del valore restituito da [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="96106-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96106-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96106-111">Return Value</span></span>

<span data-ttu-id="96106-112">Restituisce un valore intero che specifica il numero di stringhe contenute nel disco nella lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="96106-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="96106-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96106-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96106-114">Oggetto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="96106-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



