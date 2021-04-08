---
description: Il metodo SelectDefaultSubpictureLanguage imposta la lingua dell'immagine predefinita corrente nell'oggetto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Metodo SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746247"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="0c2ce-103">Metodo SelectDefaultSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="0c2ce-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="0c2ce-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0c2ce-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0c2ce-106">Il `SelectDefaultSubpictureLanguage` metodo imposta la lingua di immagine predefinita corrente nell'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="0c2ce-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="0c2ce-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c2ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c2ce-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="0c2ce-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="0c2ce-109">Specifica il linguaggio come intero.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="0c2ce-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="0c2ce-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="0c2ce-111">Specifica l'estensione del linguaggio di sottoimmagine come intero.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="0c2ce-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0c2ce-112">Value</span></span> | <span data-ttu-id="0c2ce-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c2ce-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="0c2ce-114">0</span><span class="sxs-lookup"><span data-stu-id="0c2ce-114">0</span></span>     | <span data-ttu-id="0c2ce-115">Estensione non specificata</span><span class="sxs-lookup"><span data-stu-id="0c2ce-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="0c2ce-116">1</span><span class="sxs-lookup"><span data-stu-id="0c2ce-116">1</span></span>     | <span data-ttu-id="0c2ce-117">Didascalie normali</span><span class="sxs-lookup"><span data-stu-id="0c2ce-117">Normal Captions</span></span>                |
| <span data-ttu-id="0c2ce-118">2</span><span class="sxs-lookup"><span data-stu-id="0c2ce-118">2</span></span>     | <span data-ttu-id="0c2ce-119">Didascalie grandi</span><span class="sxs-lookup"><span data-stu-id="0c2ce-119">Big Captions</span></span>                   |
| <span data-ttu-id="0c2ce-120">3</span><span class="sxs-lookup"><span data-stu-id="0c2ce-120">3</span></span>     | <span data-ttu-id="0c2ce-121">Didascalie degli elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0c2ce-121">Children's Captions</span></span>            |
| <span data-ttu-id="0c2ce-122">5</span><span class="sxs-lookup"><span data-stu-id="0c2ce-122">5</span></span>     | <span data-ttu-id="0c2ce-123">Didascalie normali chiuse</span><span class="sxs-lookup"><span data-stu-id="0c2ce-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="0c2ce-124">6</span><span class="sxs-lookup"><span data-stu-id="0c2ce-124">6</span></span>     | <span data-ttu-id="0c2ce-125">Didascalie grandi chiuse</span><span class="sxs-lookup"><span data-stu-id="0c2ce-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="0c2ce-126">7</span><span class="sxs-lookup"><span data-stu-id="0c2ce-126">7</span></span>     | <span data-ttu-id="0c2ce-127">Didascalie chiuse degli elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0c2ce-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="0c2ce-128">9</span><span class="sxs-lookup"><span data-stu-id="0c2ce-128">9</span></span>     | <span data-ttu-id="0c2ce-129">Forced</span><span class="sxs-lookup"><span data-stu-id="0c2ce-129">Forced</span></span>                         |
| <span data-ttu-id="0c2ce-130">13</span><span class="sxs-lookup"><span data-stu-id="0c2ce-130">13</span></span>    | <span data-ttu-id="0c2ce-131">Commenti del normale Director</span><span class="sxs-lookup"><span data-stu-id="0c2ce-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="0c2ce-132">14</span><span class="sxs-lookup"><span data-stu-id="0c2ce-132">14</span></span>    | <span data-ttu-id="0c2ce-133">Commenti di Big Director</span><span class="sxs-lookup"><span data-stu-id="0c2ce-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="0c2ce-134">15</span><span class="sxs-lookup"><span data-stu-id="0c2ce-134">15</span></span>    | <span data-ttu-id="0c2ce-135">Commenti del direttore per gli elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0c2ce-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c2ce-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c2ce-136">Return Value</span></span>

<span data-ttu-id="0c2ce-137">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c2ce-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c2ce-138">Remarks</span></span>

<span data-ttu-id="0c2ce-139">L'estensione del linguaggio di sottoimmagine fornisce ulteriori informazioni sulla sottoimmagine.</span><span class="sxs-lookup"><span data-stu-id="0c2ce-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



