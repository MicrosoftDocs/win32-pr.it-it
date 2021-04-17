---
description: Il metodo GetDVDTextLanguageLCID recupera l'identificatore delle impostazioni locali (LCID) per il blocco di stringhe di testo specificato.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Metodo GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520633"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="3185d-103">Metodo GetDVDTextLanguageLCID</span><span class="sxs-lookup"><span data-stu-id="3185d-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="3185d-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3185d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3185d-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="3185d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3185d-106">Il `GetDVDTextLanguageLCID` metodo recupera l'identificatore delle impostazioni locali (LCID) per il blocco di stringhe di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="3185d-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="3185d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3185d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3185d-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="3185d-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="3185d-109">Specifica il blocco di lingua del testo nel disco come intero.</span><span class="sxs-lookup"><span data-stu-id="3185d-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3185d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3185d-110">Return Value</span></span>

<span data-ttu-id="3185d-111">Restituisce un valore LCID che contiene informazioni che specificano la lingua in cui vengono scritte le stringhe.</span><span class="sxs-lookup"><span data-stu-id="3185d-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="3185d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3185d-112">Remarks</span></span>

<span data-ttu-id="3185d-113">Le stringhe di testo aggiuntive vengono archiviate in blocchi contigui sul disco. Ogni lingua ha un blocco di stringhe.</span><span class="sxs-lookup"><span data-stu-id="3185d-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="3185d-114">Un'applicazione specifica questi blocchi in base a un indice, che deve essere minore del valore restituito da [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="3185d-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3185d-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3185d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3185d-116">Oggetto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="3185d-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="3185d-117">**GetLangFromLangID**</span><span class="sxs-lookup"><span data-stu-id="3185d-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



