---
title: Costanti WINBIO_OPERATION_TYPE (tipi WinBio \_ . h)
description: Consente di specificare il tipo di operazione asincrona eseguita.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121647"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="4ec42-103">Costanti del tipo di \_ operazione WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="4ec42-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="4ec42-104">Le costanti seguenti possono essere restituite dal Windows Biometric Framework in un [**\_ \_ risultato asincrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per specificare il tipo di operazione asincrona eseguita.</span><span class="sxs-lookup"><span data-stu-id="4ec42-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="4ec42-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_operazione WINBIO \_ None**</span><span class="sxs-lookup"><span data-stu-id="4ec42-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-106">0</span><span class="sxs-lookup"><span data-stu-id="4ec42-106">0</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-107">Nessuna operazione identificata.</span><span class="sxs-lookup"><span data-stu-id="4ec42-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_operazione WINBIO \_ aperta**</span><span class="sxs-lookup"><span data-stu-id="4ec42-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-109">1</span><span class="sxs-lookup"><span data-stu-id="4ec42-109">1</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-110">È stata aperta una sessione biometrica.</span><span class="sxs-lookup"><span data-stu-id="4ec42-110">A biometric session was opened.</span></span> <span data-ttu-id="4ec42-111">Per ulteriori informazioni, vedere [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span><span class="sxs-lookup"><span data-stu-id="4ec42-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_chiusura operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-113">2</span><span class="sxs-lookup"><span data-stu-id="4ec42-113">2</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-114">Una sessione biometrica è stata chiusa.</span><span class="sxs-lookup"><span data-stu-id="4ec42-114">A biometric session was closed.</span></span> <span data-ttu-id="4ec42-115">Per ulteriori informazioni, vedere [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span><span class="sxs-lookup"><span data-stu-id="4ec42-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**\_Verifica operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-117">3</span><span class="sxs-lookup"><span data-stu-id="4ec42-117">3</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-118">È stato verificato un campione biometrico rispetto a un'identità utente.</span><span class="sxs-lookup"><span data-stu-id="4ec42-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="4ec42-119">Per ulteriori informazioni, vedere [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span><span class="sxs-lookup"><span data-stu-id="4ec42-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**\_Identificazione operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-121">4</span><span class="sxs-lookup"><span data-stu-id="4ec42-121">4</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-122">Un campione biometrico è stato acquisito e confrontato con un modello esistente.</span><span class="sxs-lookup"><span data-stu-id="4ec42-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="4ec42-123">Per ulteriori informazioni, vedere [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span><span class="sxs-lookup"><span data-stu-id="4ec42-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**\_individuazione del \_ \_ sensore nell'operazione WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-125">5</span><span class="sxs-lookup"><span data-stu-id="4ec42-125">5</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-126">Il numero di ID di un'unità biometrica è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="4ec42-127">Per ulteriori informazioni, vedere [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span><span class="sxs-lookup"><span data-stu-id="4ec42-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**\_ \_ inizio registrazione operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-129">6</span><span class="sxs-lookup"><span data-stu-id="4ec42-129">6</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-130">È stata avviata una sequenza di registrazione biometrica.</span><span class="sxs-lookup"><span data-stu-id="4ec42-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="4ec42-131">Per ulteriori informazioni, vedere [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span><span class="sxs-lookup"><span data-stu-id="4ec42-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**\_ \_ acquisizione registrazione operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-133">7</span><span class="sxs-lookup"><span data-stu-id="4ec42-133">7</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-134">Un campione biometrico è stato acquisito e aggiunto al modello.</span><span class="sxs-lookup"><span data-stu-id="4ec42-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="4ec42-135">Per ulteriori informazioni, vedere [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span><span class="sxs-lookup"><span data-stu-id="4ec42-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**\_ \_ commit registrazione operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-137">8</span><span class="sxs-lookup"><span data-stu-id="4ec42-137">8</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-138">Un modello biometrico in sospeso è stato finalizzato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="4ec42-139">Per ulteriori informazioni, vedere [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span><span class="sxs-lookup"><span data-stu-id="4ec42-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**\_eliminazione della \_ registrazione dell'operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-141">9</span><span class="sxs-lookup"><span data-stu-id="4ec42-141">9</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-142">Un modello biometrico in sospeso è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="4ec42-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="4ec42-143">Per ulteriori informazioni, vedere [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span><span class="sxs-lookup"><span data-stu-id="4ec42-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_registrazioni dell' \_ enumerazione dell'operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-145">10</span><span class="sxs-lookup"><span data-stu-id="4ec42-145">10</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-146">Sono stati enumerati i sottofattori per un determinato modello.</span><span class="sxs-lookup"><span data-stu-id="4ec42-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="4ec42-147">Per ulteriori informazioni, vedere [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span><span class="sxs-lookup"><span data-stu-id="4ec42-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**\_modello operazione di \_ eliminazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-149">11</span><span class="sxs-lookup"><span data-stu-id="4ec42-149">11</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-150">Un modello biometrico è stato eliminato dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="4ec42-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="4ec42-151">Per ulteriori informazioni, vedere [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span><span class="sxs-lookup"><span data-stu-id="4ec42-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_esempio di \_ acquisizione dell'operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-153">12</span><span class="sxs-lookup"><span data-stu-id="4ec42-153">12</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-154">È stato acquisito un campione biometrico.</span><span class="sxs-lookup"><span data-stu-id="4ec42-154">A biometric sample was captured.</span></span> <span data-ttu-id="4ec42-155">Per ulteriori informazioni, vedere [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="4ec42-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_ \_ Proprietà Get dell'operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-157">13</span><span class="sxs-lookup"><span data-stu-id="4ec42-157">13</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-158">È stata recuperata una sessione biometrica, un'unità o una proprietà di modello.</span><span class="sxs-lookup"><span data-stu-id="4ec42-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="4ec42-159">Per ulteriori informazioni, vedere [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span><span class="sxs-lookup"><span data-stu-id="4ec42-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_proprietà del \_ set di operazioni WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-161">14</span><span class="sxs-lookup"><span data-stu-id="4ec42-161">14</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-162">È stata impostata una sessione biometrica, un'unità, un modello o una proprietà dell'account.</span><span class="sxs-lookup"><span data-stu-id="4ec42-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="4ec42-163">Per ulteriori informazioni, vedere [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span><span class="sxs-lookup"><span data-stu-id="4ec42-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ evento Get operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-165">15</span><span class="sxs-lookup"><span data-stu-id="4ec42-165">15</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-166">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_unità di \_ blocco \_ operazione WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-168">16</span><span class="sxs-lookup"><span data-stu-id="4ec42-168">16</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-169">Un'unità biometrica è stata bloccata per l'uso esclusivo da una sessione.</span><span class="sxs-lookup"><span data-stu-id="4ec42-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="4ec42-170">Per ulteriori informazioni, vedere [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span><span class="sxs-lookup"><span data-stu-id="4ec42-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unità di \_ sblocco \_ operazione WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-172">17</span><span class="sxs-lookup"><span data-stu-id="4ec42-172">17</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-173">Il blocco della sessione su un'unità biometrica è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="4ec42-174">Per ulteriori informazioni, vedere [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span><span class="sxs-lookup"><span data-stu-id="4ec42-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_unità di \_ controllo dell'operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-176">18</span><span class="sxs-lookup"><span data-stu-id="4ec42-176">18</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-177">Le operazioni definite dal fornitore sono state eseguite su un'unità di controllo.</span><span class="sxs-lookup"><span data-stu-id="4ec42-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="4ec42-178">Per ulteriori informazioni, vedere [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span><span class="sxs-lookup"><span data-stu-id="4ec42-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**unità di controllo dell'operazione WINBIO con \_ \_ \_ \_ privilegi**</span><span class="sxs-lookup"><span data-stu-id="4ec42-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-180">19</span><span class="sxs-lookup"><span data-stu-id="4ec42-180">19</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-181">Le operazioni definite dal fornitore con privilegi sono state eseguite su un'unità di controllo.</span><span class="sxs-lookup"><span data-stu-id="4ec42-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="4ec42-182">Per ulteriori informazioni, vedere [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="4ec42-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ operazione di \_ apertura \_ Framework**</span><span class="sxs-lookup"><span data-stu-id="4ec42-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-184">20</span><span class="sxs-lookup"><span data-stu-id="4ec42-184">20</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-185">È stato aperto un handle per il Framework biometrico.</span><span class="sxs-lookup"><span data-stu-id="4ec42-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**\_Framework di \_ chiusura dell'operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-187">21</span><span class="sxs-lookup"><span data-stu-id="4ec42-187">21</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-188">Un handle per il Framework biometrico è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="4ec42-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="4ec42-189">Per ulteriori informazioni, vedere [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span><span class="sxs-lookup"><span data-stu-id="4ec42-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_provider di \_ \_ servizi enum operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-191">22</span><span class="sxs-lookup"><span data-stu-id="4ec42-191">22</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-192">Sono stati enumerati i provider di servizi biometrici installati.</span><span class="sxs-lookup"><span data-stu-id="4ec42-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="4ec42-193">Per ulteriori informazioni, vedere [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span><span class="sxs-lookup"><span data-stu-id="4ec42-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ unità biometriche enum operazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4ec42-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-195">23</span><span class="sxs-lookup"><span data-stu-id="4ec42-195">23</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-196">Sono state enumerate le unità biometriche collegate.</span><span class="sxs-lookup"><span data-stu-id="4ec42-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="4ec42-197">Per ulteriori informazioni, vedere [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span><span class="sxs-lookup"><span data-stu-id="4ec42-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_ \_ database enum operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-199">24</span><span class="sxs-lookup"><span data-stu-id="4ec42-199">24</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-200">I database registrati sono stati enumerati.</span><span class="sxs-lookup"><span data-stu-id="4ec42-200">The registered databases were enumerated.</span></span> <span data-ttu-id="4ec42-201">Per ulteriori informazioni, vedere [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span><span class="sxs-lookup"><span data-stu-id="4ec42-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**\_ \_ arrivo unità operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-203">25</span><span class="sxs-lookup"><span data-stu-id="4ec42-203">25</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-204">È stata creata un'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="4ec42-204">A biometric unit was created.</span></span> <span data-ttu-id="4ec42-205">Per ulteriori informazioni, vedere [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="4ec42-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**\_ \_ rimozione unità operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-207">26</span><span class="sxs-lookup"><span data-stu-id="4ec42-207">26</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-208">Un'unità biometrica è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="4ec42-208">A biometric unit was deleted.</span></span> <span data-ttu-id="4ec42-209">Per ulteriori informazioni, vedere [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="4ec42-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_ \_ identificazione \_ e rilascio del \_ \_ ticket per l'operazione WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-211">27</span><span class="sxs-lookup"><span data-stu-id="4ec42-211">27</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-212">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-212">Reserved.</span></span> <span data-ttu-id="4ec42-213">Questo valore è supportato a partire da Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ec42-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_Verifica dell'operazione WINBIO \_ \_ e \_ \_ ticket versione**</span><span class="sxs-lookup"><span data-stu-id="4ec42-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-215">28</span><span class="sxs-lookup"><span data-stu-id="4ec42-215">28</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-216">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-216">Reserved.</span></span> <span data-ttu-id="4ec42-217">Questo valore è supportato a partire da Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ec42-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_presenza di \_ monitoraggio \_ operazione WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-219">29</span><span class="sxs-lookup"><span data-stu-id="4ec42-219">29</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-220">Il meccanismo di monitoraggio del riconoscimento facciale o Iris è stato attivato.</span><span class="sxs-lookup"><span data-stu-id="4ec42-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="4ec42-221">Per ulteriori informazioni, vedere [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span><span class="sxs-lookup"><span data-stu-id="4ec42-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="4ec42-222">Questo valore è supportato a partire da Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ec42-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ec42-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**\_ \_ selezione registrazione operazione \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="4ec42-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec42-224">30</span><span class="sxs-lookup"><span data-stu-id="4ec42-224">30</span></span>
</dt> <dt>



<span data-ttu-id="4ec42-225">Un individuo di un gruppo di singoli individui rappresentati dai dati nel buffer di esempio è stato specificato come singolo da registrare.</span><span class="sxs-lookup"><span data-stu-id="4ec42-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="4ec42-226">Per ulteriori informazioni, vedere [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span><span class="sxs-lookup"><span data-stu-id="4ec42-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="4ec42-227">Questo valore è supportato a partire da Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ec42-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ec42-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ec42-228">Requirements</span></span>



| <span data-ttu-id="4ec42-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec42-229">Requirement</span></span> | <span data-ttu-id="4ec42-230">Valore</span><span class="sxs-lookup"><span data-stu-id="4ec42-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec42-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec42-231">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec42-232">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ec42-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="4ec42-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec42-233">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec42-234">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ec42-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="4ec42-235">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ec42-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ec42-236"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="4ec42-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec42-237">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ec42-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec42-238">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="4ec42-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





