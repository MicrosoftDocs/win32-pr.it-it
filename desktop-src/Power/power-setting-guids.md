---
description: I GUID dell'impostazione di risparmio energia identificano gli eventi di modifica del risparmio energia
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID dell'impostazione di risparmio energia (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332561"
---
# <a name="power-setting-guids"></a><span data-ttu-id="063a7-103">GUID dell'impostazione di risparmio energia</span><span class="sxs-lookup"><span data-stu-id="063a7-103">Power Setting GUIDs</span></span>

<span data-ttu-id="063a7-104">I **GUID** delle impostazioni di alimentazione identificano gli eventi di modifica del risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="063a7-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="063a7-105">Questo argomento elenca i **GUID** delle impostazioni di risparmio energia per le notifiche che risultano particolarmente utili per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="063a7-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="063a7-106">Un'applicazione deve registrarsi per ogni evento di modifica del risparmio di energia che può influisca sul comportamento.</span><span class="sxs-lookup"><span data-stu-id="063a7-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="063a7-107">Viene inviata una notifica ogni volta che viene modificata un'impostazione.</span><span class="sxs-lookup"><span data-stu-id="063a7-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="063a7-108">I **GUID** delle impostazioni di risparmio energia sono definiti in Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="063a7-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**\_ \_ origine alimentazione GUID \_ ACDC**</span><span class="sxs-lookup"><span data-stu-id="063a7-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span><span class="sxs-lookup"><span data-stu-id="063a7-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="063a7-111">La fonte di alimentazione del sistema è cambiata.</span><span class="sxs-lookup"><span data-stu-id="063a7-111">The system power source has changed.</span></span> <span data-ttu-id="063a7-112">Il membro **dati** è un **DWORD** con i valori dell'enumerazione della [**\_ \_ condizione di alimentazione del sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) che indica la fonte di alimentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="063a7-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-113">**PoAc** (0): il computer è alimentato da una fonte di alimentazione CA (o simile, ad esempio un portatile alimentato da una scheda 12V Automotive).</span><span class="sxs-lookup"><span data-stu-id="063a7-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="063a7-114">**PoDc** (1): il computer è alimentato da una fonte di alimentazione della batteria carica.</span><span class="sxs-lookup"><span data-stu-id="063a7-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-115">**PoHot** (2): il computer è alimentato da una fonte di alimentazione a breve termine, ad esempio un dispositivo UPS.</span><span class="sxs-lookup"><span data-stu-id="063a7-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="063a7-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**\_percentuale batteria \_ GUID \_ rimanente**</span><span class="sxs-lookup"><span data-stu-id="063a7-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="063a7-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="063a7-118">La capacità rimanente della batteria è cambiata.</span><span class="sxs-lookup"><span data-stu-id="063a7-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="063a7-119">La granularità varia da sistema a sistema, ma la granularità migliore è pari all'1%.</span><span class="sxs-lookup"><span data-stu-id="063a7-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="063a7-120">Il membro **dati** è un **valore DWORD** che indica la capacità corrente della batteria rimanente come percentuale da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="063a7-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="063a7-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**\_stato di \_ visualizzazione della console GUID \_**</span><span class="sxs-lookup"><span data-stu-id="063a7-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span><span class="sxs-lookup"><span data-stu-id="063a7-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="063a7-123">Lo stato di visualizzazione del monitoraggio corrente è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="063a7-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="063a7-124">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="063a7-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="063a7-125">Il membro **dati** è un **DWORD** con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="063a7-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-126">0x0-lo schermo è disattivato.</span><span class="sxs-lookup"><span data-stu-id="063a7-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-127">0x1: la visualizzazione è attiva.</span><span class="sxs-lookup"><span data-stu-id="063a7-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-128">0x2: la visualizzazione è visualizzata in grigio.</span><span class="sxs-lookup"><span data-stu-id="063a7-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="063a7-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_ \_ presenza utente globale \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="063a7-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span><span class="sxs-lookup"><span data-stu-id="063a7-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="063a7-131">Lo stato utente associato a una sessione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="063a7-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="063a7-132">Rappresenta lo stato combinato della presenza dell'utente in tutte le sessioni locali e remote del sistema.</span><span class="sxs-lookup"><span data-stu-id="063a7-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="063a7-133">Questa notifica viene inviata solo ai servizi e ad altri programmi in esecuzione nella sessione 0.</span><span class="sxs-lookup"><span data-stu-id="063a7-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="063a7-134">In alternativa, le applicazioni in modalità utente dovrebbero essere registrate per la **\_ \_ \_ presenza dell'utente della sessione GUID** .</span><span class="sxs-lookup"><span data-stu-id="063a7-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="063a7-135">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="063a7-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="063a7-136">Il membro **dati** è un **DWORD** con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="063a7-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-137">**PowerUserPresent** (0): l'utente è presente in una sessione locale o remota nel sistema.</span><span class="sxs-lookup"><span data-stu-id="063a7-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-138">**PowerUserInactive** (2): l'utente non è presente in alcuna sessione locale o remota nel sistema.</span><span class="sxs-lookup"><span data-stu-id="063a7-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="063a7-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_attività in \_ background INattivo GUID \_**</span><span class="sxs-lookup"><span data-stu-id="063a7-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span><span class="sxs-lookup"><span data-stu-id="063a7-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="063a7-141">Il sistema è occupato.</span><span class="sxs-lookup"><span data-stu-id="063a7-141">The system is busy.</span></span> <span data-ttu-id="063a7-142">Ciò indica che il sistema non verrà spostato in uno stato di inattività nel prossimo futuro e che l'ora corrente è un momento opportuno per i componenti per l'esecuzione di attività in background o inattive che potrebbero altrimenti impedire che il computer entri in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="063a7-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="063a7-143">Non è presente alcuna notifica quando il sistema è in grado di spostarsi in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="063a7-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="063a7-144">La notifica dell'attività in background inattiva non indica se un utente è presente nel computer.</span><span class="sxs-lookup"><span data-stu-id="063a7-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="063a7-145">Il membro **dati** non ha informazioni e può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="063a7-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="063a7-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_ \_ accensione del monitor \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="063a7-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span><span class="sxs-lookup"><span data-stu-id="063a7-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="063a7-148">Il monitoraggio di sistema primario è stato attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="063a7-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="063a7-149">Questa notifica è utile per i componenti che eseguono attivamente il rendering del contenuto nel dispositivo di visualizzazione, ad esempio la visualizzazione dei supporti.</span><span class="sxs-lookup"><span data-stu-id="063a7-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="063a7-150">Queste applicazioni devono registrarsi per questa notifica e interrompere il rendering del contenuto grafico quando il monitor è disattivato per ridurre il consumo di energia elettrica del sistema.</span><span class="sxs-lookup"><span data-stu-id="063a7-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="063a7-151">Il membro **dati** è un **valore DWORD** che indica lo stato corrente del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="063a7-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-152">0x0: il monitoraggio è disattivato.</span><span class="sxs-lookup"><span data-stu-id="063a7-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-153">0x1: il monitoraggio è on.</span><span class="sxs-lookup"><span data-stu-id="063a7-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="063a7-154">**Windows 8 e Windows Server 2012:** Le nuove applicazioni devono **usare \_ \_ \_ lo stato di visualizzazione della console GUID** invece di questa notifica.</span><span class="sxs-lookup"><span data-stu-id="063a7-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="063a7-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_ \_ stato risparmio energia \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="063a7-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="063a7-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="063a7-157">Lo screen saver batteria è stato disattivato o attivato in risposta alla modifica delle condizioni di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="063a7-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="063a7-158">Questa notifica è utile per i componenti che partecipano alla conservazione dell'energia.</span><span class="sxs-lookup"><span data-stu-id="063a7-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="063a7-159">Queste applicazioni devono registrarsi per questa notifica e risparmiare energia quando lo screen saver batteria è acceso.</span><span class="sxs-lookup"><span data-stu-id="063a7-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="063a7-160">Il membro **dati** è un **valore DWORD** che indica lo stato del risparmio di batterie.</span><span class="sxs-lookup"><span data-stu-id="063a7-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-161">0x0: il risparmio di batteria è disattivato.</span><span class="sxs-lookup"><span data-stu-id="063a7-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-162">0x1-batteria saver è attiva.</span><span class="sxs-lookup"><span data-stu-id="063a7-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="063a7-163">Risparmiare energia laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="063a7-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="063a7-164">Per informazioni generali sul risparmio di batteria, vedere [batteria saver (nelle linee guida del componente hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="063a7-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="063a7-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**\_personalità POWERSCHEME \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="063a7-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-166">245d8541-3943-4422-b025-13A784F679B7</span><span class="sxs-lookup"><span data-stu-id="063a7-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="063a7-167">La personalità dello schema di alimentazione attiva è cambiata.</span><span class="sxs-lookup"><span data-stu-id="063a7-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="063a7-168">Tutti gli schemi di risparmio energia vengono mappati a una di queste personali.</span><span class="sxs-lookup"><span data-stu-id="063a7-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="063a7-169">Il membro **dati** è un **GUID** che indica la nuova personalità dello schema di alimentazione attiva.</span><span class="sxs-lookup"><span data-stu-id="063a7-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="063a7-170">**GUID \_ \_ \_ Risparmio energetico minimo** (8C5E7FDA-E8BF-4A96-9a85-A6E23A8C635C)</span><span class="sxs-lookup"><span data-stu-id="063a7-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="063a7-171">Prestazioni elevate: lo schema è progettato per offrire le massime prestazioni a scapito del risparmio energetico.</span><span class="sxs-lookup"><span data-stu-id="063a7-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="063a7-172">**GUID \_ \_ \_ Risparmio energetico massimo** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span><span class="sxs-lookup"><span data-stu-id="063a7-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="063a7-173">Risparmio di energia: lo schema è progettato per offrire un risparmio massimo sul consumo di energia a scapito delle prestazioni e della velocità di risposta del sistema.</span><span class="sxs-lookup"><span data-stu-id="063a7-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="063a7-174">**GUID \_ \_ \_ Risparmio energetico tipico** (381B4222-F694-41f0-9685-FF5BB260DF2E)</span><span class="sxs-lookup"><span data-stu-id="063a7-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="063a7-175">Automatico: lo schema è progettato per bilanciare automaticamente le prestazioni e il risparmio del consumo di energia.</span><span class="sxs-lookup"><span data-stu-id="063a7-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="063a7-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**\_stato di \_ visualizzazione della sessione GUID \_**</span><span class="sxs-lookup"><span data-stu-id="063a7-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span><span class="sxs-lookup"><span data-stu-id="063a7-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="063a7-178">Lo schermo associato alla sessione dell'applicazione è stato attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="063a7-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="063a7-179">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="063a7-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="063a7-180">Questa notifica viene inviata solo alle applicazioni in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="063a7-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="063a7-181">I servizi e gli altri programmi in esecuzione nella sessione 0 non ricevono questa notifica.</span><span class="sxs-lookup"><span data-stu-id="063a7-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="063a7-182">Il membro **dati** è un **DWORD** con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="063a7-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-183">0x0-lo schermo è disattivato.</span><span class="sxs-lookup"><span data-stu-id="063a7-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-184">0x1: la visualizzazione è attiva.</span><span class="sxs-lookup"><span data-stu-id="063a7-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-185">0x2: la visualizzazione è visualizzata in grigio.</span><span class="sxs-lookup"><span data-stu-id="063a7-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="063a7-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**\_ \_ presenza utente della sessione GUID \_**</span><span class="sxs-lookup"><span data-stu-id="063a7-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span><span class="sxs-lookup"><span data-stu-id="063a7-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="063a7-188">Lo stato utente associato alla sessione dell'applicazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="063a7-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="063a7-189">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa notifica è disponibile a partire da Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="063a7-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="063a7-190">Questa notifica viene inviata solo alle applicazioni in modalità utente in esecuzione in una sessione interattiva.</span><span class="sxs-lookup"><span data-stu-id="063a7-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="063a7-191">I servizi e gli altri programmi in esecuzione nella sessione 0 devono essere registrati per la **\_ \_ \_ presenza di utenti globali GUID**.</span><span class="sxs-lookup"><span data-stu-id="063a7-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="063a7-192">Il membro **dati** è un **DWORD** con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="063a7-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-193">**PowerUserPresent** (0): l'utente fornisce l'input per la sessione.</span><span class="sxs-lookup"><span data-stu-id="063a7-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-194">**PowerUserInactive** (2): il timeout dell'attività utente è scaduto senza alcuna interazione da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="063a7-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="063a7-195">Tutte le applicazioni eseguite in una sessione interattiva in modalità utente devono usare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="063a7-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="063a7-196">Quando le applicazioni in modalità kernel si registrano per lo stato del monitoraggio, è consigliabile utilizzare **\_ \_ \_ lo stato di visualizzazione della console GUID** .</span><span class="sxs-lookup"><span data-stu-id="063a7-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="063a7-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**\_modalità utente assente di sistema GUID \_**</span><span class="sxs-lookup"><span data-stu-id="063a7-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="063a7-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span><span class="sxs-lookup"><span data-stu-id="063a7-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="063a7-199">Il sistema è in entrata o in uscita dalla modalità.</span><span class="sxs-lookup"><span data-stu-id="063a7-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="063a7-200">Il membro **dati** è un **valore DWORD** che indica lo stato della modalità di disvia corrente.</span><span class="sxs-lookup"><span data-stu-id="063a7-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="063a7-201">0x0: il computer sta uscendo dalla modalità.</span><span class="sxs-lookup"><span data-stu-id="063a7-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="063a7-202">0x1-il computer sta entrando in modalità di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="063a7-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="063a7-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="063a7-203">Requirements</span></span>



| <span data-ttu-id="063a7-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="063a7-204">Requirement</span></span> | <span data-ttu-id="063a7-205">Valore</span><span class="sxs-lookup"><span data-stu-id="063a7-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="063a7-206">Intestazione</span><span class="sxs-lookup"><span data-stu-id="063a7-206">Header</span></span><br/> | <dl> <span data-ttu-id="063a7-207"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="063a7-207"><dt>WinNT.h</dt></span></span> </dl> |



 

