---
description: Aggiorna il messaggio di rinnovabilità del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226516"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="7f56e-103">\_set OPM \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="7f56e-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="7f56e-104">Aggiorna il messaggio di rinnovabilità del sistema (SRM) per High-Bandwidth Digital protezione del contenuto (HDCP).</span><span class="sxs-lookup"><span data-stu-id="7f56e-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="7f56e-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f56e-105">Requirement</span></span> | <span data-ttu-id="7f56e-106">Valore</span><span class="sxs-lookup"><span data-stu-id="7f56e-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f56e-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="7f56e-107">Command GUID</span></span> | <span data-ttu-id="7f56e-108">\_set OPM \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="7f56e-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="7f56e-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="7f56e-109">Input data</span></span>   | <span data-ttu-id="7f56e-110">Struttura di parametri di un [**set di OPM \_ \_ \_ SRM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)</span><span class="sxs-lookup"><span data-stu-id="7f56e-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="7f56e-111">Il parametro *pbAdditionalParameters* di [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) deve puntare a un buffer che contiene SRM.</span><span class="sxs-lookup"><span data-stu-id="7f56e-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="7f56e-112">Il formato di un SRM SRM è documentato nella specifica HDCP.</span><span class="sxs-lookup"><span data-stu-id="7f56e-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="7f56e-113">Impostare il parametro *ulAdditionalParametersSize* in modo che corrisponda alla dimensione del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="7f56e-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f56e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f56e-114">Remarks</span></span>

<span data-ttu-id="7f56e-115">SRM vengono usati per aggiornare l'elenco dei dispositivi HDCP revocati.</span><span class="sxs-lookup"><span data-stu-id="7f56e-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="7f56e-116">SRM vengono forniti con il contenuto video.</span><span class="sxs-lookup"><span data-stu-id="7f56e-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="7f56e-117">Questo comando Aggiorna l'SRM corrente dell'output del video.</span><span class="sxs-lookup"><span data-stu-id="7f56e-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="7f56e-118">Se la funzionalità HDCP è abilitata al momento del comando, l'output del video usa il nuovo SRM per verificare se uno dei dispositivi HDCP connessi viene revocato.</span><span class="sxs-lookup"><span data-stu-id="7f56e-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="7f56e-119">Se l'output del video rileva un dispositivo revocato, smette di visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="7f56e-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="7f56e-120">Se si invia questo comando mentre HDCP è disabilitato, l'output del video convalida l'SRM e lo archivia.</span><span class="sxs-lookup"><span data-stu-id="7f56e-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="7f56e-121">In seguito, se l'applicazione Abilita HDCP, l'output del video usa il nuovo SRM per verificare lo stato di revoca del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f56e-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="7f56e-122">Questo comando può causare la restituzione da parte del metodo **Configure** dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="7f56e-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="7f56e-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7f56e-123">Return code</span></span>                                            | <span data-ttu-id="7f56e-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f56e-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="7f56e-125">ERRORE della \_ grafica \_ OPM \_ non valido \_ SRM</span><span class="sxs-lookup"><span data-stu-id="7f56e-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="7f56e-126">SRM non è valido.</span><span class="sxs-lookup"><span data-stu-id="7f56e-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="7f56e-127">ERRORE \_ l' \_ output OPM della grafica non \_ \_ \_ \_ supporta \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="7f56e-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="7f56e-128">L'output del video non supporta la HDCP.</span><span class="sxs-lookup"><span data-stu-id="7f56e-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="7f56e-129">Questo comando non è supportato quando l'interfaccia **IOPMVideoOutput** emula il protocollo COPP (Certified Output Protection).</span><span class="sxs-lookup"><span data-stu-id="7f56e-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="7f56e-130">Quando si usano la semantica COPP, l'applicazione è responsabile dell'analisi di SRM e del controllo dello stato di revoca del dispositivo HDCP.</span><span class="sxs-lookup"><span data-stu-id="7f56e-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="7f56e-131">Usare la richiesta di stato delle [ \_ \_ \_ \_ \_ informazioni sul dispositivo HDCP Get Connected](opm-get-connected-hdcp-device-information.md) per ottenere il vettore di selezione chiavi del dispositivo (KSV), necessario per controllare lo stato di revoca.</span><span class="sxs-lookup"><span data-stu-id="7f56e-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="7f56e-132">Per altre informazioni su SRM, vedere la specifica HDCP.</span><span class="sxs-lookup"><span data-stu-id="7f56e-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f56e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f56e-133">Requirements</span></span>



| <span data-ttu-id="7f56e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f56e-134">Requirement</span></span> | <span data-ttu-id="7f56e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7f56e-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f56e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f56e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7f56e-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f56e-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7f56e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f56e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7f56e-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f56e-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f56e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f56e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f56e-141"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f56e-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f56e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f56e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f56e-143">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="7f56e-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="7f56e-144">Comandi di OPM</span><span class="sxs-lookup"><span data-stu-id="7f56e-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




