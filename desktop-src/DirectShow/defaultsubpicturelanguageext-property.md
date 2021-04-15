---
description: Tramite la proprietà DefaultSubpictureLanguageExt viene recuperata l'estensione predefinita per il linguaggio dell'immagine di DVD.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Proprietà DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520746"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="02bc9-103">Proprietà DefaultSubpictureLanguageExt</span><span class="sxs-lookup"><span data-stu-id="02bc9-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="02bc9-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="02bc9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="02bc9-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="02bc9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="02bc9-106">Tramite la `DefaultSubpictureLanguageExt` proprietà viene recuperata l'estensione predefinita per il linguaggio della sottoimmagine DVD.</span><span class="sxs-lookup"><span data-stu-id="02bc9-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="02bc9-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02bc9-107">Return Value</span></span>

<span data-ttu-id="02bc9-108">Restituisce un valore intero che indica l'estensione predefinita per il linguaggio di sottoimmagine DVD.</span><span class="sxs-lookup"><span data-stu-id="02bc9-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="02bc9-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="02bc9-109">Remarks</span></span>

<span data-ttu-id="02bc9-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="02bc9-110">This property is read-only with no default value.</span></span> <span data-ttu-id="02bc9-111">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="02bc9-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="02bc9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="02bc9-112">Value</span></span> | <span data-ttu-id="02bc9-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02bc9-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="02bc9-114">0</span><span class="sxs-lookup"><span data-stu-id="02bc9-114">0</span></span>     | <span data-ttu-id="02bc9-115">Estensione non specificata</span><span class="sxs-lookup"><span data-stu-id="02bc9-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="02bc9-116">1</span><span class="sxs-lookup"><span data-stu-id="02bc9-116">1</span></span>     | <span data-ttu-id="02bc9-117">Didascalie normali</span><span class="sxs-lookup"><span data-stu-id="02bc9-117">Normal Captions</span></span>                |
| <span data-ttu-id="02bc9-118">2</span><span class="sxs-lookup"><span data-stu-id="02bc9-118">2</span></span>     | <span data-ttu-id="02bc9-119">Didascalie grandi</span><span class="sxs-lookup"><span data-stu-id="02bc9-119">Big Captions</span></span>                   |
| <span data-ttu-id="02bc9-120">3</span><span class="sxs-lookup"><span data-stu-id="02bc9-120">3</span></span>     | <span data-ttu-id="02bc9-121">Didascalie degli elementi figlio</span><span class="sxs-lookup"><span data-stu-id="02bc9-121">Children's Captions</span></span>            |
| <span data-ttu-id="02bc9-122">5</span><span class="sxs-lookup"><span data-stu-id="02bc9-122">5</span></span>     | <span data-ttu-id="02bc9-123">Didascalie normali chiuse</span><span class="sxs-lookup"><span data-stu-id="02bc9-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="02bc9-124">6</span><span class="sxs-lookup"><span data-stu-id="02bc9-124">6</span></span>     | <span data-ttu-id="02bc9-125">Didascalie grandi chiuse</span><span class="sxs-lookup"><span data-stu-id="02bc9-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="02bc9-126">7</span><span class="sxs-lookup"><span data-stu-id="02bc9-126">7</span></span>     | <span data-ttu-id="02bc9-127">Didascalie chiuse degli elementi figlio</span><span class="sxs-lookup"><span data-stu-id="02bc9-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="02bc9-128">9</span><span class="sxs-lookup"><span data-stu-id="02bc9-128">9</span></span>     | <span data-ttu-id="02bc9-129">Forced</span><span class="sxs-lookup"><span data-stu-id="02bc9-129">Forced</span></span>                         |
| <span data-ttu-id="02bc9-130">13</span><span class="sxs-lookup"><span data-stu-id="02bc9-130">13</span></span>    | <span data-ttu-id="02bc9-131">Commenti del normale Director</span><span class="sxs-lookup"><span data-stu-id="02bc9-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="02bc9-132">14</span><span class="sxs-lookup"><span data-stu-id="02bc9-132">14</span></span>    | <span data-ttu-id="02bc9-133">Commenti di Big Director</span><span class="sxs-lookup"><span data-stu-id="02bc9-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="02bc9-134">15</span><span class="sxs-lookup"><span data-stu-id="02bc9-134">15</span></span>    | <span data-ttu-id="02bc9-135">Commenti del direttore per gli elementi figlio</span><span class="sxs-lookup"><span data-stu-id="02bc9-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="02bc9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02bc9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02bc9-137">**SelectDefaultSubpictureLanguage**</span><span class="sxs-lookup"><span data-stu-id="02bc9-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



