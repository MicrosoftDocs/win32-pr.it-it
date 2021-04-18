---
description: Imposta il livello di protezione per un meccanismo di protezione dell'output.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309049"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="f51f8-103">\_livello di \_ protezione \_ set OPM</span><span class="sxs-lookup"><span data-stu-id="f51f8-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="f51f8-104">Imposta il livello di protezione per un meccanismo di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="f51f8-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="f51f8-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51f8-105">Requirement</span></span> | <span data-ttu-id="f51f8-106">Valore</span><span class="sxs-lookup"><span data-stu-id="f51f8-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51f8-107">GUID comando</span><span class="sxs-lookup"><span data-stu-id="f51f8-107">Command GUID</span></span> | <span data-ttu-id="f51f8-108">\_livello di \_ protezione \_ set OPM</span><span class="sxs-lookup"><span data-stu-id="f51f8-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="f51f8-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="f51f8-109">Input data</span></span>   | <span data-ttu-id="f51f8-110">Struttura [**di \_ \_ parametri del \_ livello \_ di protezione set di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="f51f8-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f51f8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f51f8-111">Remarks</span></span>

<span data-ttu-id="f51f8-112">Alcuni connettori possono supportare più meccanismi di protezione.</span><span class="sxs-lookup"><span data-stu-id="f51f8-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="f51f8-113">Con questo tipo di connettore, è possibile applicare diversi meccanismi di protezione allo stesso connettore, con impostazioni diverse per ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="f51f8-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51f8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f51f8-114">Requirements</span></span>



| <span data-ttu-id="f51f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51f8-115">Requirement</span></span> | <span data-ttu-id="f51f8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f51f8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f51f8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f51f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f51f8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f51f8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f51f8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f51f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f51f8-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f51f8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f51f8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f51f8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f51f8-122"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f51f8-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f51f8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f51f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51f8-124">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="f51f8-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="f51f8-125">Comandi di OPM</span><span class="sxs-lookup"><span data-stu-id="f51f8-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




