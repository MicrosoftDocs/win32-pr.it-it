---
description: Modifica la modalità di avvio di un oggetto servizio derivato da Win32 \_ BaseService.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: Metodo ChangeStartMode della classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126687"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="e7e8b-103">Metodo ChangeStartMode della \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="e7e8b-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="e7e8b-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica la modalità di avvio di un oggetto servizio derivato da [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e7e8b-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="e7e8b-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e7e8b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e7e8b-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e7e8b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e8b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7e8b-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="e7e8b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7e8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e8b-109">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e8b-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-110">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="e7e8b-111">Il valore predefinito è "Automatic".</span><span class="sxs-lookup"><span data-stu-id="e7e8b-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="e7e8b-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="e7e8b-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="e7e8b-113">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e7e8b-114">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="e7e8b-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="e7e8b-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="e7e8b-116">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e7e8b-117">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="e7e8b-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="e7e8b-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="e7e8b-119">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="e7e8b-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="e7e8b-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="e7e8b-121">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e8b-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e7e8b-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="e7e8b-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="e7e8b-123">Il servizio è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e8b-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7e8b-124">Return value</span></span>

<span data-ttu-id="e7e8b-125">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e7e8b-126">**Success**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-127">0</span><span class="sxs-lookup"><span data-stu-id="e7e8b-127">0</span></span>

<span data-ttu-id="e7e8b-128">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-129">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-130">1</span><span class="sxs-lookup"><span data-stu-id="e7e8b-130">1</span></span>

<span data-ttu-id="e7e8b-131">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-132">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-133">2</span><span class="sxs-lookup"><span data-stu-id="e7e8b-133">2</span></span>

<span data-ttu-id="e7e8b-134">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-135">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-136">3</span><span class="sxs-lookup"><span data-stu-id="e7e8b-136">3</span></span>

<span data-ttu-id="e7e8b-137">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-138">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-139">4</span><span class="sxs-lookup"><span data-stu-id="e7e8b-139">4</span></span>

<span data-ttu-id="e7e8b-140">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-141">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-142">5</span><span class="sxs-lookup"><span data-stu-id="e7e8b-142">5</span></span>

<span data-ttu-id="e7e8b-143">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio (proprietà di [**stato**](win32-baseservice.md) [**\_ BaseService Win32**](win32-baseservice.md)) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-144">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-145">6</span><span class="sxs-lookup"><span data-stu-id="e7e8b-145">6</span></span>

<span data-ttu-id="e7e8b-146">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-147">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-148">7</span><span class="sxs-lookup"><span data-stu-id="e7e8b-148">7</span></span>

<span data-ttu-id="e7e8b-149">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-150">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-151">8</span><span class="sxs-lookup"><span data-stu-id="e7e8b-151">8</span></span>

<span data-ttu-id="e7e8b-152">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-153">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-154">9</span><span class="sxs-lookup"><span data-stu-id="e7e8b-154">9</span></span>

<span data-ttu-id="e7e8b-155">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-156">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-157">10</span><span class="sxs-lookup"><span data-stu-id="e7e8b-157">10</span></span>

<span data-ttu-id="e7e8b-158">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-159">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-160">11</span><span class="sxs-lookup"><span data-stu-id="e7e8b-160">11</span></span>

<span data-ttu-id="e7e8b-161">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-162">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-163">12</span><span class="sxs-lookup"><span data-stu-id="e7e8b-163">12</span></span>

<span data-ttu-id="e7e8b-164">Il servizio si basa su una dipendenza che è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-165">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-166">13</span><span class="sxs-lookup"><span data-stu-id="e7e8b-166">13</span></span>

<span data-ttu-id="e7e8b-167">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-168">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-169">14</span><span class="sxs-lookup"><span data-stu-id="e7e8b-169">14</span></span>

<span data-ttu-id="e7e8b-170">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-171">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-172">15</span><span class="sxs-lookup"><span data-stu-id="e7e8b-172">15</span></span>

<span data-ttu-id="e7e8b-173">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-174">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-175">16</span><span class="sxs-lookup"><span data-stu-id="e7e8b-175">16</span></span>

<span data-ttu-id="e7e8b-176">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-177">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-178">17</span><span class="sxs-lookup"><span data-stu-id="e7e8b-178">17</span></span>

<span data-ttu-id="e7e8b-179">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-180">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-181">18</span><span class="sxs-lookup"><span data-stu-id="e7e8b-181">18</span></span>

<span data-ttu-id="e7e8b-182">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-183">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-184">19</span><span class="sxs-lookup"><span data-stu-id="e7e8b-184">19</span></span>

<span data-ttu-id="e7e8b-185">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-186">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-187">20</span><span class="sxs-lookup"><span data-stu-id="e7e8b-187">20</span></span>

<span data-ttu-id="e7e8b-188">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-189">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-190">21</span><span class="sxs-lookup"><span data-stu-id="e7e8b-190">21</span></span>

<span data-ttu-id="e7e8b-191">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-192">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-193">22</span><span class="sxs-lookup"><span data-stu-id="e7e8b-193">22</span></span>

<span data-ttu-id="e7e8b-194">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-195">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-196">23</span><span class="sxs-lookup"><span data-stu-id="e7e8b-196">23</span></span>

<span data-ttu-id="e7e8b-197">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-198">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-199">24</span><span class="sxs-lookup"><span data-stu-id="e7e8b-199">24</span></span>

<span data-ttu-id="e7e8b-200">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e8b-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="e7e8b-201">**Altri**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e7e8b-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="e7e8b-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7e8b-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7e8b-203">Requirements</span></span>



| <span data-ttu-id="e7e8b-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7e8b-204">Requirement</span></span> | <span data-ttu-id="e7e8b-205">Valore</span><span class="sxs-lookup"><span data-stu-id="e7e8b-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e8b-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7e8b-206">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e8b-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7e8b-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7e8b-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7e8b-208">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e8b-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e8b-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7e8b-210">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7e8b-210">Namespace</span></span><br/>                | <span data-ttu-id="e7e8b-211">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e7e8b-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7e8b-212">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e8b-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e8b-213"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7e8b-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e8b-214">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e8b-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e8b-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e8b-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e8b-216">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7e8b-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7e8b-217">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7e8b-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e7e8b-218">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="e7e8b-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

