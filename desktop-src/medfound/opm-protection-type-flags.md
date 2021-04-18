---
description: I flag nella tabella seguente specificano i meccanismi di protezione dell'output per l'output Protection Manager (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Flag del tipo di protezione OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309051"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="09b92-103">Flag del tipo di protezione OPM</span><span class="sxs-lookup"><span data-stu-id="09b92-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="09b92-104">I flag nella tabella seguente specificano i meccanismi di protezione dell'output per l'output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="09b92-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="09b92-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="09b92-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="09b92-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09b92-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="09b92-107"><dt>**OPM \_ Tipo di protezione \_ \_ altri**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="09b92-108">Meccanismo di protezione sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="09b92-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="09b92-109"><dt>**OPM \_ Tipo di protezione \_ \_ None**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="09b92-110">Nessun meccanismo di protezione.</span><span class="sxs-lookup"><span data-stu-id="09b92-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="09b92-111"><dt>**OPM \_ Tipo di protezione \_ \_ Copp \_ compatibile con 0x00000001 \_ HDCP**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="09b92-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="09b92-112">High-Bandwidth protezione del contenuto digitali (HDCP).</span><span class="sxs-lookup"><span data-stu-id="09b92-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="09b92-113">Questo flag viene utilizzato per l'emulazione di COPP (Certified Output Protocol).</span><span class="sxs-lookup"><span data-stu-id="09b92-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="09b92-114">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="09b92-114">For more information, see Remarks.</span></span> <span data-ttu-id="09b92-115">Questo flag non è supportato per la semantica di OPM.</span><span class="sxs-lookup"><span data-stu-id="09b92-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="09b92-116"><dt>**OPM \_ Tipo di protezione \_ \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="09b92-117">Protezione copia analoga (ACP).</span><span class="sxs-lookup"><span data-stu-id="09b92-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="09b92-118"><dt>**OPM \_ Tipo di protezione \_ \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="09b92-119">Sistema di gestione della generazione di copia: analogico (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="09b92-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="09b92-120"><dt>**OPM \_ Tipo di protezione \_ \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="09b92-121">Protocollo HDCP.</span><span class="sxs-lookup"><span data-stu-id="09b92-121">HDCP.</span></span> <span data-ttu-id="09b92-122">Questo flag viene usato quando l'oggetto OPM ha la semantica OPM.</span><span class="sxs-lookup"><span data-stu-id="09b92-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="09b92-123">Non è supportata per la semantica COPP.</span><span class="sxs-lookup"><span data-stu-id="09b92-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="09b92-124"><dt>**OPM \_ Tipo di protezione \_ \_ DPCP**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="09b92-125">DisplayPort protezione del contenuto (DPCP).</span><span class="sxs-lookup"><span data-stu-id="09b92-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="09b92-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="09b92-126">Remarks</span></span>

<span data-ttu-id="09b92-127">Questi flag vengono usati nei seguenti comandi e richieste di stato di OPM.</span><span class="sxs-lookup"><span data-stu-id="09b92-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="09b92-128">\_livello di \_ protezione \_ set OPM</span><span class="sxs-lookup"><span data-stu-id="09b92-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="09b92-129">\_livello di \_ \_ protezione virtuale \_ di OPM Get</span><span class="sxs-lookup"><span data-stu-id="09b92-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="09b92-130">OPM \_ ottenere \_ il \_ livello di protezione effettivo \_</span><span class="sxs-lookup"><span data-stu-id="09b92-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="09b92-131">PROTOCOLLO HDCP</span><span class="sxs-lookup"><span data-stu-id="09b92-131">HDCP</span></span>

<span data-ttu-id="09b92-132">I due flag seguenti sono definiti per HDCP.</span><span class="sxs-lookup"><span data-stu-id="09b92-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="09b92-133">Valore</span><span class="sxs-lookup"><span data-stu-id="09b92-133">Value</span></span>                                         | <span data-ttu-id="09b92-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09b92-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b92-135">tipo di protezione di OPM \_ \_ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="09b92-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="09b92-136">Usare questo flag se il puntatore [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) è stato creato con la semantica OPM.</span><span class="sxs-lookup"><span data-stu-id="09b92-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="09b92-137">\_tipo di protezione OPM \_ \_ Copp \_ compatibile con \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="09b92-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="09b92-138">Utilizzare questo flag se il puntatore [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) è stato creato con la semantica di Copp.</span><span class="sxs-lookup"><span data-stu-id="09b92-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="09b92-139">Questo flag corrisponde al flag COPP \_ ProtectionType \_ HDCP in copp.</span><span class="sxs-lookup"><span data-stu-id="09b92-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="09b92-140">Entrambe le modalità (semantica OPM e semantica COPP) supportano le operazioni seguenti per HDCP:</span><span class="sxs-lookup"><span data-stu-id="09b92-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="09b92-141">Abilitare o disabilitare HDCP usando il comando [OPM \_ set \_ Protection \_ Level](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="09b92-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="09b92-142">Eseguire una query per verificare se la funzionalità HDCP è abilitata usando la richiesta di stato del livello di protezione ( [OPM \_ get \_ virtual \_ Protection \_ ](opm-get-virtual-protection-level.md) ) o [OPM \_ get \_ actual \_ \_ ](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="09b92-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="09b92-143">La semantica di OPM supporta inoltre quanto segue:</span><span class="sxs-lookup"><span data-stu-id="09b92-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="09b92-144">Ripetitori HDCP.</span><span class="sxs-lookup"><span data-stu-id="09b92-144">HDCP repeaters.</span></span> <span data-ttu-id="09b92-145">Un *Repeater HDCP* è un dispositivo HDCP che può ricevere contenuti HDCP e anche crittografare nuovamente e trasmettere lo stesso contenuto.</span><span class="sxs-lookup"><span data-stu-id="09b92-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="09b92-146">Revoca HDCP.</span><span class="sxs-lookup"><span data-stu-id="09b92-146">HDCP revocation.</span></span> <span data-ttu-id="09b92-147">Se un dispositivo HDCP revocato viene collegato all'output del video OPM, l'output del video non trasmette il video.</span><span class="sxs-lookup"><span data-stu-id="09b92-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="09b92-148">Non è necessario che l'applicazione analizzi i messaggi di rinnovabilità del sistema HDCP (SRM) o determini se il dispositivo di output è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="09b92-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="09b92-149">Per altre informazioni, vedere il comando [**OPM \_ set \_ HDCP \_ MSR**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="09b92-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="09b92-150">Quando si usano la semantica COPP, l'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) non supporta i ripetitori HDCP.</span><span class="sxs-lookup"><span data-stu-id="09b92-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="09b92-151">Non gestisce inoltre la revoca HDCP.</span><span class="sxs-lookup"><span data-stu-id="09b92-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="09b92-152">Al contrario, l'applicazione deve analizzare l'SRM per determinare se un dispositivo HDCP è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="09b92-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b92-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09b92-153">Requirements</span></span>



| <span data-ttu-id="09b92-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="09b92-154">Requirement</span></span> | <span data-ttu-id="09b92-155">Valore</span><span class="sxs-lookup"><span data-stu-id="09b92-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09b92-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09b92-156">Minimum supported client</span></span><br/> | <span data-ttu-id="09b92-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09b92-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="09b92-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09b92-158">Minimum supported server</span></span><br/> | <span data-ttu-id="09b92-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09b92-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09b92-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09b92-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="09b92-161"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09b92-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b92-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09b92-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b92-163">Enumerazioni di OPM</span><span class="sxs-lookup"><span data-stu-id="09b92-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




