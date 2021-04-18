---
description: Le costanti flag globali vengono usate per abilitare o disabilitare le opzioni dei criteri di risparmio energia dell'utente.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Costanti flag globali (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312049"
---
# <a name="global-flags-constants"></a><span data-ttu-id="8ca83-103">Costanti flag globali</span><span class="sxs-lookup"><span data-stu-id="8ca83-103">Global Flags Constants</span></span>

<span data-ttu-id="8ca83-104">Le costanti flag globali vengono usate per abilitare o disabilitare le opzioni dei criteri di risparmio energia dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8ca83-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="8ca83-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="8ca83-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="8ca83-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca83-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="8ca83-107"><dt></dt> <dt>0x02</dt> EnableMultiBatteryDisplay</span><span class="sxs-lookup"><span data-stu-id="8ca83-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="8ca83-108">Abilita o Disabilita lo schermo a più batterie nel contatore di alimentazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="8ca83-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="8ca83-109"><dt></dt> <dt>0x04</dt> EnablePasswordLogon</span><span class="sxs-lookup"><span data-stu-id="8ca83-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="8ca83-110">Abilita o Disabilita la richiesta di accesso con password quando il sistema riprende dalla modalità standby o di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="8ca83-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="8ca83-111"><dt></dt> <dt>0x01</dt> EnableSysTrayBatteryMeter</span><span class="sxs-lookup"><span data-stu-id="8ca83-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="8ca83-112">Abilita o Disabilita l'icona del contatore della batteria nella barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8ca83-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="8ca83-113">Quando questo flag è deselezionato, l'icona del contatore della batteria non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="8ca83-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="8ca83-114"><dt></dt> <dt>0x10</dt> EnableVideoDimDisplay</span><span class="sxs-lookup"><span data-stu-id="8ca83-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="8ca83-115">Abilita o Disabilita il supporto per l'attenuazione dello schermo video quando il sistema passa dall'esecuzione a alimentazione a batteria elettrica.</span><span class="sxs-lookup"><span data-stu-id="8ca83-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="8ca83-116"><dt></dt> <dt>0x08</dt> EnableWakeOnRing</span><span class="sxs-lookup"><span data-stu-id="8ca83-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="8ca83-117">Abilita o Disabilita il supporto per riattivazione ring.</span><span class="sxs-lookup"><span data-stu-id="8ca83-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="8ca83-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ca83-118">Requirements</span></span>



| <span data-ttu-id="8ca83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca83-119">Requirement</span></span> | <span data-ttu-id="8ca83-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca83-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca83-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca83-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8ca83-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8ca83-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca83-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ca83-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ca83-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ca83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca83-126"><dt>PowrProf. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca83-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca83-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ca83-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca83-128">**\_criteri di \_ risparmio energia utente globale \_**</span><span class="sxs-lookup"><span data-stu-id="8ca83-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




