---
title: DVD. disponibile
description: La proprietà disavailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | DVD. disponibile
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. Media Player Windows disponibile
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321399"
---
# <a name="dvdisavailable"></a><span data-ttu-id="6726b-105">DVD. disponibile</span><span class="sxs-lookup"><span data-stu-id="6726b-105">DVD.isAvailable</span></span>

<span data-ttu-id="6726b-106">La proprietà **disavailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="6726b-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="6726b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6726b-107">Parameters</span></span>

<span data-ttu-id="6726b-108">*nome*</span><span class="sxs-lookup"><span data-stu-id="6726b-108">*name*</span></span>

<span data-ttu-id="6726b-109">**Stringa** contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6726b-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="6726b-110">string</span><span class="sxs-lookup"><span data-stu-id="6726b-110">String</span></span>     | <span data-ttu-id="6726b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6726b-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6726b-112">Indietro</span><span class="sxs-lookup"><span data-stu-id="6726b-112">back</span></span>       | <span data-ttu-id="6726b-113">Determina se il metodo **indietro** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6726b-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="6726b-114">DVD</span><span class="sxs-lookup"><span data-stu-id="6726b-114">dvd</span></span>        | <span data-ttu-id="6726b-115">Determina se il DVD è caricato.</span><span class="sxs-lookup"><span data-stu-id="6726b-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="6726b-116">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="6726b-116">dvdDecoder</span></span> | <span data-ttu-id="6726b-117">Determina se il decoder DVD è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6726b-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="6726b-118">resume</span><span class="sxs-lookup"><span data-stu-id="6726b-118">resume</span></span>     | <span data-ttu-id="6726b-119">Determina se il metodo **Resume** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6726b-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="6726b-120">titleMenu</span><span class="sxs-lookup"><span data-stu-id="6726b-120">titleMenu</span></span>  | <span data-ttu-id="6726b-121">Determina se il metodo **titleMenu** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6726b-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="6726b-122">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="6726b-122">topMenu</span></span>    | <span data-ttu-id="6726b-123">Determina se il metodo **tomenu** è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6726b-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="6726b-124">Comunemente chiamato menu radice.</span><span class="sxs-lookup"><span data-stu-id="6726b-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="6726b-125">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="6726b-125">Return Values</span></span>

<span data-ttu-id="6726b-126">Questo metodo restituisce un **valore booleano** di sola lettura che indica se il parametro specificato è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6726b-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="6726b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="6726b-127">Remarks</span></span>

<span data-ttu-id="6726b-128">Le funzionalità DVD di Windows Media Player non funzioneranno nei computer in cui non sono installati decodificatori DVD di terze parti.</span><span class="sxs-lookup"><span data-stu-id="6726b-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="6726b-129">È possibile determinare se un decodificatore **è disponibile chiamando l'oggetto ("** dvdDecoder").</span><span class="sxs-lookup"><span data-stu-id="6726b-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="6726b-130">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="6726b-130">Every DVD is authored differently.</span></span> <span data-ttu-id="6726b-131">I metodi disponibili durante la riproduzione e la navigazione in DVD dipendono dal modo in cui viene creato il DVD.</span><span class="sxs-lookup"><span data-stu-id="6726b-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="6726b-132">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre **false**.</span><span class="sxs-lookup"><span data-stu-id="6726b-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6726b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6726b-133">Requirements</span></span>



| <span data-ttu-id="6726b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6726b-134">Requirement</span></span> | <span data-ttu-id="6726b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6726b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6726b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6726b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6726b-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6726b-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6726b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6726b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6726b-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6726b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6726b-140">Versione</span><span class="sxs-lookup"><span data-stu-id="6726b-140">Version</span></span><br/>                  | <span data-ttu-id="6726b-141">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6726b-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="6726b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6726b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6726b-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6726b-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6726b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6726b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6726b-145">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="6726b-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





