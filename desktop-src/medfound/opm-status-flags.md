---
description: I flag nella tabella seguente specificano lo stato di una sessione di output Protection Manager (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Flag di stato OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527871"
---
# <a name="opm-status-flags"></a><span data-ttu-id="40f3f-103">Flag di stato OPM</span><span class="sxs-lookup"><span data-stu-id="40f3f-103">OPM Status Flags</span></span>

<span data-ttu-id="40f3f-104">I flag nella tabella seguente specificano lo stato di una sessione di output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="40f3f-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="40f3f-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="40f3f-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="40f3f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40f3f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="40f3f-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="40f3f-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40f3f-108">Stato normale.</span><span class="sxs-lookup"><span data-stu-id="40f3f-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="40f3f-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="40f3f-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40f3f-110">L'integrità della connessione è stata compromessa.</span><span class="sxs-lookup"><span data-stu-id="40f3f-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="40f3f-111">Di seguito sono riportati alcuni esempi di eventi che determinano l'impostazione di questo flag da parte del driver:</span><span class="sxs-lookup"><span data-stu-id="40f3f-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="40f3f-112">Il driver non può più applicare il livello di protezione corrente.</span><span class="sxs-lookup"><span data-stu-id="40f3f-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="40f3f-113">Il driver ha rilevato un errore di integrità interna.</span><span class="sxs-lookup"><span data-stu-id="40f3f-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="40f3f-114">Il connettore tra il computer e il dispositivo di visualizzazione è stato scollegato.</span><span class="sxs-lookup"><span data-stu-id="40f3f-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="40f3f-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="40f3f-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40f3f-116">La configurazione della connessione è cambiata.</span><span class="sxs-lookup"><span data-stu-id="40f3f-116">The connection configuration has changed.</span></span> <span data-ttu-id="40f3f-117">Ad esempio, l'utente ha modificato la modalità di visualizzazione del desktop.</span><span class="sxs-lookup"><span data-stu-id="40f3f-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="40f3f-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="40f3f-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40f3f-119">La scheda grafica o il driver è stato manomesso.</span><span class="sxs-lookup"><span data-stu-id="40f3f-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="40f3f-120">Questo flag non viene usato in <em>modalità di emulazione Copp</em>.</span><span class="sxs-lookup"><span data-stu-id="40f3f-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="40f3f-121">Al contrario, l'output del video imposterà il flag di OPM_STATUS_LINK_LOST se rileva manomissioni.</span><span class="sxs-lookup"><span data-stu-id="40f3f-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="40f3f-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="40f3f-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="40f3f-123">Un dispositivo con High-Bandwidth protezione del contenuto digitale revocato (HDCP) viene collegato all'output del video.</span><span class="sxs-lookup"><span data-stu-id="40f3f-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="40f3f-124">Questo flag di stato può essere restituito da una query <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> o <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> .</span><span class="sxs-lookup"><span data-stu-id="40f3f-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="40f3f-125">Il dispositivo revocato potrebbe essere collegato direttamente all'output del video o indirettamente tramite un Repeater HDCP.</span><span class="sxs-lookup"><span data-stu-id="40f3f-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="40f3f-126">È necessario un output video per rilevare questa condizione mentre è abilitata la funzionalità HDCP, ma non in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="40f3f-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="40f3f-127">Questo flag non viene usato in <em>modalità di emulazione Copp</em>, perché l'output del video non rileva i dispositivi revocati in tale modalità.</span><span class="sxs-lookup"><span data-stu-id="40f3f-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="40f3f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="40f3f-128">Remarks</span></span>

<span data-ttu-id="40f3f-129">Alcune di queste costanti sono equivalenti ai valori dell'enumerazione **Copp \_ StatusFlags** utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="40f3f-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="40f3f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40f3f-130">Requirements</span></span>



| <span data-ttu-id="40f3f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f3f-131">Requirement</span></span> | <span data-ttu-id="40f3f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="40f3f-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40f3f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40f3f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="40f3f-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40f3f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="40f3f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40f3f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="40f3f-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40f3f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="40f3f-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40f3f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f3f-138"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f3f-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f3f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40f3f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f3f-140">Enumerazioni di OPM</span><span class="sxs-lookup"><span data-stu-id="40f3f-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




