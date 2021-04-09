---
title: Costanti WINBIO_BIR_PURPOSE (tipi WinBio \_ . h)
description: Specificare lo scopo a cui è destinato il record di informazioni biometriche (BIR) o per cui è adatto.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964276"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="63e63-103">Costanti WINBIO per \_ \_ finalità Bir</span><span class="sxs-lookup"><span data-stu-id="63e63-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="63e63-104">I flag seguenti vengono usati dal membro **scopo** della struttura dell' [**\_ \_ intestazione WINBIO bir**](winbio-bir-header.md) per specificare lo scopo per cui è previsto il record di informazioni biometriche (Bir) o per cui è adatto.</span><span class="sxs-lookup"><span data-stu-id="63e63-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="63e63-105">Costante</span><span class="sxs-lookup"><span data-stu-id="63e63-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="63e63-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63e63-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="63e63-107"><dt>**WINBIO \_ senza \_ scopo \_ disponibile**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="63e63-108">Nessun scopo specificato.</span><span class="sxs-lookup"><span data-stu-id="63e63-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="63e63-109"><dt>**\_Verifica finalità \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="63e63-110">Verificare l'identità di un utente.</span><span class="sxs-lookup"><span data-stu-id="63e63-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="63e63-111"><dt>**\_Identificazione scopo \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="63e63-112">Identificare un utente.</span><span class="sxs-lookup"><span data-stu-id="63e63-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="63e63-113"><dt>**\_registrazione scopo \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="63e63-114">Registrare un utente.</span><span class="sxs-lookup"><span data-stu-id="63e63-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="63e63-115"><dt>**\_registrazione scopo \_ WINBIO \_ per la \_ Verifica**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="63e63-116">Acquisire un campione biometrico e determinare se l'esempio corrisponde all'identità utente specificata.</span><span class="sxs-lookup"><span data-stu-id="63e63-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="63e63-117"><dt>**\_registrazione scopo \_ WINBIO \_ per l' \_ Identificazione**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="63e63-118">Acquisire un campione biometrico e determinare se corrisponde a un modello biometrico esistente.</span><span class="sxs-lookup"><span data-stu-id="63e63-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="63e63-119"><dt>**\_controllo scopo \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="63e63-120">Informazioni aggiuntive che possono essere usate per la registrazione o per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="63e63-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="63e63-121">Questo valore viene ignorato nell'input da tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="63e63-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="63e63-122">Nell'output sarà disponibile solo se supportata dall'unità biometrica e si specifica il flag di **\_ dati WINBIO \_ \_ RAW** nel parametro *Flags* della funzione [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .</span><span class="sxs-lookup"><span data-stu-id="63e63-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="63e63-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63e63-123">Requirements</span></span>



| <span data-ttu-id="63e63-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e63-124">Requirement</span></span> | <span data-ttu-id="63e63-125">Valore</span><span class="sxs-lookup"><span data-stu-id="63e63-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e63-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63e63-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63e63-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63e63-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="63e63-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63e63-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63e63-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="63e63-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="63e63-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63e63-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="63e63-131"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63e63-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e63-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63e63-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e63-133">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="63e63-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="63e63-134">**\_intestazione WINBIO bir \_**</span><span class="sxs-lookup"><span data-stu-id="63e63-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





