---
description: Usare i flag di opzione seguenti per specificare che il programma di installazione non scrive il valore immesso nel campo di destinazione della tabella CustomAction nel log. Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo Type della tabella CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opzione di destinazione nascosta azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050155"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="b4005-104">Opzione di destinazione nascosta azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b4005-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="b4005-105">Usare i flag di opzione seguenti per specificare che il programma di installazione non scrive il valore immesso nel campo di destinazione della [tabella CustomAction](customaction-table.md) nel log.</span><span class="sxs-lookup"><span data-stu-id="b4005-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="b4005-106">Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo Type della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="b4005-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="b4005-107">Costante</span><span class="sxs-lookup"><span data-stu-id="b4005-107">Constant</span></span>                            | <span data-ttu-id="b4005-108">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b4005-108">Hexadecimal</span></span> | <span data-ttu-id="b4005-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="b4005-109">Decimal</span></span> | <span data-ttu-id="b4005-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4005-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4005-111">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="b4005-111">(none)</span></span>                              | <span data-ttu-id="b4005-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="b4005-112">0x0000</span></span>      | <span data-ttu-id="b4005-113">0</span><span class="sxs-lookup"><span data-stu-id="b4005-113">0</span></span>       | <span data-ttu-id="b4005-114">Il programma di installazione può scrivere il valore nella colonna di destinazione della tabella CustomAction nel file di log.</span><span class="sxs-lookup"><span data-stu-id="b4005-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b4005-115">**msidbCustomActionTypeHideTarget**</span><span class="sxs-lookup"><span data-stu-id="b4005-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="b4005-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="b4005-116">0x2000</span></span>      | <span data-ttu-id="b4005-117">8192</span><span class="sxs-lookup"><span data-stu-id="b4005-117">8192</span></span>    | <span data-ttu-id="b4005-118">Al programma di installazione non è consentito scrivere il valore nella colonna di destinazione della [tabella CustomAction](customaction-table.md) nel file di log.</span><span class="sxs-lookup"><span data-stu-id="b4005-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="b4005-119">Inoltre, la proprietà CustomActionData non viene registrata quando il programma di installazione esegue l'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b4005-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="b4005-120">Poiché il programma di installazione imposta il valore di CustomActionData da una proprietà con lo stesso nome dell'azione personalizzata, tale proprietà deve essere elencata nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) per impedire che il relativo valore venga visualizzato nel log.</span><span class="sxs-lookup"><span data-stu-id="b4005-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="b4005-121">Per ulteriori informazioni, vedere la pagina relativa alla [prevenzione della scrittura di informazioni riservate nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md)</span><span class="sxs-lookup"><span data-stu-id="b4005-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4005-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4005-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4005-123">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="b4005-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="b4005-124">Informazioni sulle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="b4005-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="b4005-125">Uso di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="b4005-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




