---
description: Il metodo SelectDefaultAudioLanguage imposta la lingua audio predefinita corrente nell'oggetto MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Metodo SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521274"
---
# <a name="selectdefaultaudiolanguage-method"></a><span data-ttu-id="e9e6b-103">Metodo SelectDefaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="e9e6b-103">SelectDefaultAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="e9e6b-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9e6b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e9e6b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9e6b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e9e6b-106">Il `SelectDefaultAudioLanguage` metodo imposta la lingua audio predefinita corrente nell'oggetto mswebdvd.</span><span class="sxs-lookup"><span data-stu-id="e9e6b-106">The `SelectDefaultAudioLanguage` method sets the current default audio language in the MSWebDVD object.</span></span>

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a><span data-ttu-id="e9e6b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9e6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e6b-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="e9e6b-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="e9e6b-109">Specifica la lingua come valore LCID di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="e9e6b-109">Specifies the language as an Integer LCID value.</span></span>

</dd> <dt>

<span data-ttu-id="e9e6b-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="e9e6b-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="e9e6b-111">Specifica l'estensione di lingua audio DVD come valore intero.</span><span class="sxs-lookup"><span data-stu-id="e9e6b-111">Specifies the DVD audio language extension as an integer value.</span></span>



| <span data-ttu-id="e9e6b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e6b-112">Value</span></span> | <span data-ttu-id="e9e6b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9e6b-113">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="e9e6b-114">0</span><span class="sxs-lookup"><span data-stu-id="e9e6b-114">0</span></span>     | <span data-ttu-id="e9e6b-115">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="e9e6b-115">NotSpecified</span></span>      |
| <span data-ttu-id="e9e6b-116">1</span><span class="sxs-lookup"><span data-stu-id="e9e6b-116">1</span></span>     | <span data-ttu-id="e9e6b-117">Sottotitoli</span><span class="sxs-lookup"><span data-stu-id="e9e6b-117">Captions</span></span>          |
| <span data-ttu-id="e9e6b-118">2</span><span class="sxs-lookup"><span data-stu-id="e9e6b-118">2</span></span>     | <span data-ttu-id="e9e6b-119">VisuallyImpaired</span><span class="sxs-lookup"><span data-stu-id="e9e6b-119">VisuallyImpaired</span></span>  |
| <span data-ttu-id="e9e6b-120">3</span><span class="sxs-lookup"><span data-stu-id="e9e6b-120">3</span></span>     | <span data-ttu-id="e9e6b-121">DirectorComments1</span><span class="sxs-lookup"><span data-stu-id="e9e6b-121">DirectorComments1</span></span> |
| <span data-ttu-id="e9e6b-122">4</span><span class="sxs-lookup"><span data-stu-id="e9e6b-122">4</span></span>     | <span data-ttu-id="e9e6b-123">DirectorComments2</span><span class="sxs-lookup"><span data-stu-id="e9e6b-123">DirectorComments2</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e6b-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9e6b-124">Return Value</span></span>

<span data-ttu-id="e9e6b-125">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e9e6b-125">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9e6b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9e6b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e6b-127">Oggetto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="e9e6b-127">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



