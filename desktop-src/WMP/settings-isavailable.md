---
title: Settings. available
description: La proprietà disavailable indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. | Settings. available
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Impostazioni. Media Player Windows disponibile
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327382"
---
# <a name="settingsisavailable"></a><span data-ttu-id="ba90d-105">Settings. available</span><span class="sxs-lookup"><span data-stu-id="ba90d-105">Settings.isAvailable</span></span>

<span data-ttu-id="ba90d-106">La proprietà **disavailable** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="ba90d-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba90d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba90d-107">Syntax</span></span>

<span data-ttu-id="ba90d-108">Player. Settings. available (nome)</span><span class="sxs-lookup"><span data-stu-id="ba90d-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="ba90d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba90d-109">Parameters</span></span>

<span data-ttu-id="ba90d-110">*nome*</span><span class="sxs-lookup"><span data-stu-id="ba90d-110">*name*</span></span>

<span data-ttu-id="ba90d-111">Stringa contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ba90d-111">String containing one of the following values.</span></span>



| <span data-ttu-id="ba90d-112">string</span><span class="sxs-lookup"><span data-stu-id="ba90d-112">String</span></span>             | <span data-ttu-id="ba90d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba90d-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="ba90d-114">avvio automatico</span><span class="sxs-lookup"><span data-stu-id="ba90d-114">AutoStart</span></span>          | <span data-ttu-id="ba90d-115">Determina se è possibile impostare la proprietà di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="ba90d-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="ba90d-116">Balance</span><span class="sxs-lookup"><span data-stu-id="ba90d-116">Balance</span></span>            | <span data-ttu-id="ba90d-117">Determina se è possibile impostare la proprietà Balance.</span><span class="sxs-lookup"><span data-stu-id="ba90d-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="ba90d-118">BaseURL</span><span class="sxs-lookup"><span data-stu-id="ba90d-118">BaseURL</span></span>            | <span data-ttu-id="ba90d-119">Determina se è possibile impostare la proprietà baseURL.</span><span class="sxs-lookup"><span data-stu-id="ba90d-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="ba90d-120">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="ba90d-120">DefaultFrame</span></span>       | <span data-ttu-id="ba90d-121">Determina se è possibile impostare la proprietà defaultFrame.</span><span class="sxs-lookup"><span data-stu-id="ba90d-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="ba90d-122">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="ba90d-122">EnableErrorDialogs</span></span> | <span data-ttu-id="ba90d-123">Determina se è possibile impostare la proprietà enableErrorDialogs.</span><span class="sxs-lookup"><span data-stu-id="ba90d-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="ba90d-124">GetMode</span><span class="sxs-lookup"><span data-stu-id="ba90d-124">GetMode</span></span>            | <span data-ttu-id="ba90d-125">Determina se è possibile chiamare il metodo GetMode.</span><span class="sxs-lookup"><span data-stu-id="ba90d-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="ba90d-126">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="ba90d-126">InvokeURLs</span></span>         | <span data-ttu-id="ba90d-127">Determina se è possibile impostare la proprietà invokeURLs.</span><span class="sxs-lookup"><span data-stu-id="ba90d-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="ba90d-128">Disattiva audio</span><span class="sxs-lookup"><span data-stu-id="ba90d-128">Mute</span></span>               | <span data-ttu-id="ba90d-129">Determina se è possibile impostare la proprietà mute.</span><span class="sxs-lookup"><span data-stu-id="ba90d-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="ba90d-130">PlayCount</span><span class="sxs-lookup"><span data-stu-id="ba90d-130">PlayCount</span></span>          | <span data-ttu-id="ba90d-131">Determina se è possibile impostare la proprietà playCount.</span><span class="sxs-lookup"><span data-stu-id="ba90d-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="ba90d-132">Tariffa</span><span class="sxs-lookup"><span data-stu-id="ba90d-132">Rate</span></span>               | <span data-ttu-id="ba90d-133">Determina se è possibile impostare la proprietà rate.</span><span class="sxs-lookup"><span data-stu-id="ba90d-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="ba90d-134">SetMode</span><span class="sxs-lookup"><span data-stu-id="ba90d-134">SetMode</span></span>            | <span data-ttu-id="ba90d-135">Determina se è possibile chiamare il metodo semode.</span><span class="sxs-lookup"><span data-stu-id="ba90d-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="ba90d-136">Volume</span><span class="sxs-lookup"><span data-stu-id="ba90d-136">Volume</span></span>             | <span data-ttu-id="ba90d-137">Determina se è possibile impostare la proprietà del volume.</span><span class="sxs-lookup"><span data-stu-id="ba90d-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="ba90d-138">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="ba90d-138">Return Values</span></span>

<span data-ttu-id="ba90d-139">Questo metodo restituisce un valore **booleano** .</span><span class="sxs-lookup"><span data-stu-id="ba90d-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba90d-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba90d-140">Requirements</span></span>



| <span data-ttu-id="ba90d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba90d-141">Requirement</span></span> | <span data-ttu-id="ba90d-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ba90d-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba90d-143">Versione</span><span class="sxs-lookup"><span data-stu-id="ba90d-143">Version</span></span><br/> | <span data-ttu-id="ba90d-144">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ba90d-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ba90d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ba90d-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba90d-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba90d-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba90d-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba90d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba90d-148">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="ba90d-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





