---
description: Questi flag specificano il comportamento del localizzatore multimediale.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Flag di convalida del nome file (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327925"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="1b51c-103">Flag di convalida del nome file</span><span class="sxs-lookup"><span data-stu-id="1b51c-103">File Name Validation Flags</span></span>

<span data-ttu-id="1b51c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1b51c-104">\[Deprecated.</span></span> <span data-ttu-id="1b51c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1b51c-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="1b51c-106">Questi flag specificano il comportamento del localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="1b51c-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="1b51c-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="1b51c-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="1b51c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b51c-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="1b51c-109"><dt>**SFN \_ \_Controllo VALIDATEF**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="1b51c-110">Verificare la validità dei nomi file.</span><span class="sxs-lookup"><span data-stu-id="1b51c-110">Check the validity of file names.</span></span> <span data-ttu-id="1b51c-111">È necessario impostare questo flag per convalidare i nomi dei file.</span><span class="sxs-lookup"><span data-stu-id="1b51c-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="1b51c-112">In caso contrario, gli altri flag non hanno alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1b51c-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="1b51c-113"><dt>**SFN \_ 0x02 \_ popup VALIDATEF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="1b51c-114">Se un file non è disponibile, visualizzare una finestra di dialogo Apri file per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="1b51c-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="1b51c-115"><dt>**SFN \_ VALIDATEF \_**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="1b51c-116">Se viene individuato un file mancante, visualizzare brevemente una finestra di messaggio con il nome e il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="1b51c-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="1b51c-117">Questo flag è particolarmente utile a scopo di test. la finestra di messaggio non è probabilmente adatta per un prodotto finale.</span><span class="sxs-lookup"><span data-stu-id="1b51c-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="1b51c-118"><dt>**SFN \_ VALIDATEF \_ sostituire**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="1b51c-119">Se viene individuato un file mancante, aggiornare il nome dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="1b51c-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="1b51c-120">(Valido solo nel metodo [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).</span><span class="sxs-lookup"><span data-stu-id="1b51c-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="1b51c-121"><dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="1b51c-122">Usare sempre un file locale, anche se nella rete è presente una versione del file.</span><span class="sxs-lookup"><span data-stu-id="1b51c-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="1b51c-123"><dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="1b51c-124">Non cercare i file mancanti.</span><span class="sxs-lookup"><span data-stu-id="1b51c-124">Do not search for missing files.</span></span> <span data-ttu-id="1b51c-125">Se si imposta il flag di controllo VALIDATEF SFN, i nomi dei file vengono ancora convalidati \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b51c-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="1b51c-126"><dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="1b51c-127">Ignorare gli oggetti di origine silenziati.</span><span class="sxs-lookup"><span data-stu-id="1b51c-127">Ignore muted source objects.</span></span> <span data-ttu-id="1b51c-128">(Valido solo nel metodo [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).</span><span class="sxs-lookup"><span data-stu-id="1b51c-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="1b51c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b51c-129">Requirements</span></span>



| <span data-ttu-id="1b51c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b51c-130">Requirement</span></span> | <span data-ttu-id="1b51c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1b51c-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b51c-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b51c-132">Header</span></span><br/> | <dl> <span data-ttu-id="1b51c-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b51c-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b51c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b51c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b51c-135">**IMediaLocator::FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="1b51c-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="1b51c-136">**IRenderEngine::SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="1b51c-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




