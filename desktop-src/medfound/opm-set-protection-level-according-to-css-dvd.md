---
description: Imposta il livello di protezione HDCP per la riproduzione DVD, seguendo le regole CSS (Content Scramble System) del DVD.
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130494"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="3fb41-103">\_impostazione del \_ \_ livello di protezione di OPM \_ \_ in base al \_ \_ DVD CSS</span><span class="sxs-lookup"><span data-stu-id="3fb41-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="3fb41-104">Imposta il livello di protezione HDCP per la riproduzione DVD, seguendo le regole CSS (Content Scramble System) del DVD.</span><span class="sxs-lookup"><span data-stu-id="3fb41-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="3fb41-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb41-105">Requirement</span></span> | <span data-ttu-id="3fb41-106">Valore</span><span class="sxs-lookup"><span data-stu-id="3fb41-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb41-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="3fb41-107">Command GUID</span></span> | <span data-ttu-id="3fb41-108">\_impostazione del \_ \_ livello di protezione di OPM \_ \_ in base al \_ \_ DVD CSS</span><span class="sxs-lookup"><span data-stu-id="3fb41-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="3fb41-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="3fb41-109">Input data</span></span>   | <span data-ttu-id="3fb41-110">Struttura [**di \_ \_ parametri del \_ livello \_ di protezione set di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="3fb41-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3fb41-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fb41-111">Remarks</span></span>

<span data-ttu-id="3fb41-112">Questo comando viene usato per impostare High-Bandwidth Digital protezione del contenuto (HDCP) quando si esegue la riproduzione di DVD standard.</span><span class="sxs-lookup"><span data-stu-id="3fb41-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="3fb41-113">A differenza del comando di [**\_ impostazione del \_ \_ livello di protezione di OPM**](opm-set-protection-level.md) , se non è possibile impostare HDCP per qualche motivo, questo comando non interrompe la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3fb41-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="3fb41-114">(Le regole CSS DVD contengono un provisioning "Best Effort" per i giocatori). In caso contrario, questo comando è identico al comando **OPM \_ set \_ Protection \_ Level** .</span><span class="sxs-lookup"><span data-stu-id="3fb41-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb41-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fb41-115">Requirements</span></span>



| <span data-ttu-id="3fb41-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb41-116">Requirement</span></span> | <span data-ttu-id="3fb41-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3fb41-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb41-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb41-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fb41-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3fb41-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb41-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3fb41-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3fb41-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fb41-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb41-123"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb41-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb41-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fb41-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb41-125">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="3fb41-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="3fb41-126">Comandi di OPM</span><span class="sxs-lookup"><span data-stu-id="3fb41-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




