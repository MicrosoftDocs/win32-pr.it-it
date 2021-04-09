---
description: Il metodo GetLangFromLangID recupera una stringa leggibile quando viene specificato un ID di lingua primario.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Metodo GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876542"
---
# <a name="getlangfromlangid-method"></a><span data-ttu-id="6f0e6-103">Metodo GetLangFromLangID</span><span class="sxs-lookup"><span data-stu-id="6f0e6-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="6f0e6-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6f0e6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6f0e6-106">Il `GetLangFromLangID` metodo recupera una stringa leggibile quando viene specificato un ID di lingua primario.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="6f0e6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f0e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f0e6-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span><span class="sxs-lookup"><span data-stu-id="6f0e6-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="6f0e6-109">Specifica l'ID della lingua primaria come intero.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f0e6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f0e6-110">Return Value</span></span>

<span data-ttu-id="6f0e6-111">Restituisce una rappresentazione di stringa del linguaggio che può essere visualizzato nell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f0e6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f0e6-112">Remarks</span></span>

<span data-ttu-id="6f0e6-113">Sebbene questo metodo sia denominato `GetLangFromLangID` , il parametro passato è in realtà l'ID della lingua primaria, non l'ID della lingua.</span><span class="sxs-lookup"><span data-stu-id="6f0e6-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f0e6-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f0e6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0e6-115">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="6f0e6-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="6f0e6-116">**GetDVDTextLanguageLCID**</span><span class="sxs-lookup"><span data-stu-id="6f0e6-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



