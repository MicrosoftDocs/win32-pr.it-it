---
description: '\\Pannello di controllo HKCU \\ internazionale.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877453"
---
# <a name="addhijridate"></a><span data-ttu-id="2acad-103">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="2acad-103">AddHijriDate</span></span>

<span data-ttu-id="2acad-104">**\\Pannello di controllo HKCU \\ internazionale**</span><span class="sxs-lookup"><span data-stu-id="2acad-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="2acad-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2acad-105">Data type</span></span> | <span data-ttu-id="2acad-106">Range</span><span class="sxs-lookup"><span data-stu-id="2acad-106">Range</span></span>                      | <span data-ttu-id="2acad-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="2acad-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="2acad-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="2acad-108">REG\_SZ</span></span>   | <span data-ttu-id="2acad-109">*Valore di regolazione valido*</span><span class="sxs-lookup"><span data-stu-id="2acad-109">*A valid adjustment value*</span></span> | <span data-ttu-id="2acad-110">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="2acad-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="2acad-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2acad-111">Description</span></span>

<span data-ttu-id="2acad-112">Specifica le modifiche alla data nel calendario Hijri.</span><span class="sxs-lookup"><span data-stu-id="2acad-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="2acad-113">Il calendario Hijri è un calendario lunare usato nel mondo islamico.</span><span class="sxs-lookup"><span data-stu-id="2acad-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="2acad-114">I mesi iniziano e terminano in base a un decreto che si basa sull'osservazione della nuova luna.</span><span class="sxs-lookup"><span data-stu-id="2acad-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="2acad-115">È difficile prevedere accuratamente gli inizi e le terminazioni dei mesi e sono presenti variazioni internazionali, quindi viene apportata una modifica tra zero e due giorni al calendario.</span><span class="sxs-lookup"><span data-stu-id="2acad-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="2acad-116">Il valore del registro di sistema **AddHijriDate** archivia questo valore di regolazione come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2acad-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="2acad-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2acad-117">Value</span></span>          | <span data-ttu-id="2acad-118">Significato</span><span class="sxs-lookup"><span data-stu-id="2acad-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acad-119">AddHijriDate-2</span><span class="sxs-lookup"><span data-stu-id="2acad-119">AddHijriDate-2</span></span> | <span data-ttu-id="2acad-120">Sottrarre due giorni.</span><span class="sxs-lookup"><span data-stu-id="2acad-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="2acad-121">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="2acad-121">AddHijriDate</span></span>   | <span data-ttu-id="2acad-122">Sottrarre un giorno.</span><span class="sxs-lookup"><span data-stu-id="2acad-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="2acad-123">(vuoto)</span><span class="sxs-lookup"><span data-stu-id="2acad-123">(blank)</span></span>        | <span data-ttu-id="2acad-124">Non è necessaria alcuna regolazione.</span><span class="sxs-lookup"><span data-stu-id="2acad-124">No adjustment is necessary.</span></span> <span data-ttu-id="2acad-125">Se la data non è stata modificata, questa voce non viene visualizzata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2acad-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="2acad-126">Se la data è stata modificata e quindi ripristinata al valore originale, questa voce viene visualizzata nel registro di sistema senza alcun valore.</span><span class="sxs-lookup"><span data-stu-id="2acad-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="2acad-127">AddHijriDate + 1</span><span class="sxs-lookup"><span data-stu-id="2acad-127">AddHijriDate+1</span></span> | <span data-ttu-id="2acad-128">Aggiungere un giorno.</span><span class="sxs-lookup"><span data-stu-id="2acad-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="2acad-129">AddHijriDate + 2</span><span class="sxs-lookup"><span data-stu-id="2acad-129">AddHijriDate+2</span></span> | <span data-ttu-id="2acad-130">Aggiungere due giorni.</span><span class="sxs-lookup"><span data-stu-id="2acad-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="2acad-131">Questa voce non è disponibile nel Registro di sistema per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2acad-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="2acad-132">È possibile aggiungerlo utilizzando l'editor del registro di sistema Regedit.exe o utilizzando il metodo di modifica descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="2acad-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="2acad-133">Cambia metodo</span><span class="sxs-lookup"><span data-stu-id="2acad-133">Change Method</span></span>

<span data-ttu-id="2acad-134">Per modificare il valore di questa voce o per aggiungerlo al registro di sistema, installare prima i file per le lingue con alfabeti non latini e con scrittura da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="2acad-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="2acad-135">Nel pannello di controllo fare clic su **Opzioni internazionali e della lingua**, quindi fare clic sulla scheda **lingue** . In **supporto lingua supplementare** selezionare la casella di controllo per **installare i file per le lingue con alfabeti non latini e da destra a sinistra (incluso Thai)**.</span><span class="sxs-lookup"><span data-stu-id="2acad-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="2acad-136">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="2acad-136">Click **OK**.</span></span>

<span data-ttu-id="2acad-137">Per modificare il valore di questa voce o per aggiungerlo al registro di sistema, nel pannello di controllo fare clic su **Opzioni internazionali e della lingua**.</span><span class="sxs-lookup"><span data-stu-id="2acad-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="2acad-138">Nel campo **standard e formati** selezionare le impostazioni locali che utilizzano il calendario Hijri.</span><span class="sxs-lookup"><span data-stu-id="2acad-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="2acad-139">Fare clic sul pulsante **Personalizza** , quindi sulla scheda **Data** . Nell'elenco a discesa **Adjust date Hijri to:** selezionare il valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="2acad-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="2acad-140">Fare clic su **OK**, quindi fare di nuovo clic su **OK** .</span><span class="sxs-lookup"><span data-stu-id="2acad-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="2acad-141">Metodo di attivazione</span><span class="sxs-lookup"><span data-stu-id="2acad-141">Activation Method</span></span>

<span data-ttu-id="2acad-142">Le modifiche apportate a questa voce tramite il pannello di controllo hanno effetto immediato.</span><span class="sxs-lookup"><span data-stu-id="2acad-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



