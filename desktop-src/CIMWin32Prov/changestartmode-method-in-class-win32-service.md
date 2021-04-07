---
description: Modifica la modalità di avvio di un \_ servizio Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Metodo ChangeStartMode della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049173"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="00d04-103">Metodo ChangeStartMode della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="00d04-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="00d04-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica la modalità di avvio di un [**\_ servizio Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="00d04-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="00d04-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="00d04-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="00d04-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="00d04-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="00d04-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d04-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="00d04-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="00d04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d04-109">*StartMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00d04-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d04-110">Modalità di avvio del servizio di base di Windows.</span><span class="sxs-lookup"><span data-stu-id="00d04-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="00d04-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")</span><span class="sxs-lookup"><span data-stu-id="00d04-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="00d04-112">Driver di dispositivo avviato dal caricatore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="00d04-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="00d04-113">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="00d04-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="00d04-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="00d04-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="00d04-115">Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="00d04-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="00d04-116">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="00d04-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="00d04-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="00d04-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="00d04-118">Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="00d04-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="00d04-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="00d04-120">Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="00d04-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="00d04-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")</span><span class="sxs-lookup"><span data-stu-id="00d04-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="00d04-122">Servizio che non può più essere avviato.</span><span class="sxs-lookup"><span data-stu-id="00d04-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d04-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00d04-123">Return value</span></span>

<span data-ttu-id="00d04-124">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="00d04-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="00d04-125">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="00d04-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="00d04-126">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="00d04-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="00d04-127">**Success**</span><span class="sxs-lookup"><span data-stu-id="00d04-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-128">0</span><span class="sxs-lookup"><span data-stu-id="00d04-128">0</span></span>

<span data-ttu-id="00d04-129">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="00d04-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-130">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="00d04-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-131">1</span><span class="sxs-lookup"><span data-stu-id="00d04-131">1</span></span>

<span data-ttu-id="00d04-132">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="00d04-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-133">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="00d04-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-134">2</span><span class="sxs-lookup"><span data-stu-id="00d04-134">2</span></span>

<span data-ttu-id="00d04-135">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="00d04-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-136">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="00d04-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-137">3</span><span class="sxs-lookup"><span data-stu-id="00d04-137">3</span></span>

<span data-ttu-id="00d04-138">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-139">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="00d04-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-140">4</span><span class="sxs-lookup"><span data-stu-id="00d04-140">4</span></span>

<span data-ttu-id="00d04-141">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-142">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="00d04-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-143">5</span><span class="sxs-lookup"><span data-stu-id="00d04-143">5</span></span>

<span data-ttu-id="00d04-144">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="00d04-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-145">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="00d04-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-146">6</span><span class="sxs-lookup"><span data-stu-id="00d04-146">6</span></span>

<span data-ttu-id="00d04-147">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="00d04-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-148">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="00d04-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-149">7</span><span class="sxs-lookup"><span data-stu-id="00d04-149">7</span></span>

<span data-ttu-id="00d04-150">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="00d04-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-151">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="00d04-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-152">8</span><span class="sxs-lookup"><span data-stu-id="00d04-152">8</span></span>

<span data-ttu-id="00d04-153">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-154">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="00d04-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-155">9</span><span class="sxs-lookup"><span data-stu-id="00d04-155">9</span></span>

<span data-ttu-id="00d04-156">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-157">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="00d04-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-158">10</span><span class="sxs-lookup"><span data-stu-id="00d04-158">10</span></span>

<span data-ttu-id="00d04-159">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="00d04-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-160">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="00d04-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-161">11</span><span class="sxs-lookup"><span data-stu-id="00d04-161">11</span></span>

<span data-ttu-id="00d04-162">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="00d04-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-163">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="00d04-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-164">12</span><span class="sxs-lookup"><span data-stu-id="00d04-164">12</span></span>

<span data-ttu-id="00d04-165">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-166">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="00d04-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-167">13</span><span class="sxs-lookup"><span data-stu-id="00d04-167">13</span></span>

<span data-ttu-id="00d04-168">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="00d04-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-169">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="00d04-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-170">14</span><span class="sxs-lookup"><span data-stu-id="00d04-170">14</span></span>

<span data-ttu-id="00d04-171">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-172">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="00d04-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-173">15</span><span class="sxs-lookup"><span data-stu-id="00d04-173">15</span></span>

<span data-ttu-id="00d04-174">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-175">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="00d04-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-176">16</span><span class="sxs-lookup"><span data-stu-id="00d04-176">16</span></span>

<span data-ttu-id="00d04-177">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-178">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="00d04-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-179">17</span><span class="sxs-lookup"><span data-stu-id="00d04-179">17</span></span>

<span data-ttu-id="00d04-180">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="00d04-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-181">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="00d04-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-182">18</span><span class="sxs-lookup"><span data-stu-id="00d04-182">18</span></span>

<span data-ttu-id="00d04-183">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="00d04-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-184">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="00d04-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-185">19</span><span class="sxs-lookup"><span data-stu-id="00d04-185">19</span></span>

<span data-ttu-id="00d04-186">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="00d04-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-187">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="00d04-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-188">20</span><span class="sxs-lookup"><span data-stu-id="00d04-188">20</span></span>

<span data-ttu-id="00d04-189">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="00d04-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-190">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="00d04-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-191">21</span><span class="sxs-lookup"><span data-stu-id="00d04-191">21</span></span>

<span data-ttu-id="00d04-192">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-193">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="00d04-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-194">22</span><span class="sxs-lookup"><span data-stu-id="00d04-194">22</span></span>

<span data-ttu-id="00d04-195">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-196">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="00d04-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-197">23</span><span class="sxs-lookup"><span data-stu-id="00d04-197">23</span></span>

<span data-ttu-id="00d04-198">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-199">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="00d04-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-200">24</span><span class="sxs-lookup"><span data-stu-id="00d04-200">24</span></span>

<span data-ttu-id="00d04-201">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="00d04-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="00d04-202">**Altri**</span><span class="sxs-lookup"><span data-stu-id="00d04-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="00d04-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="00d04-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="00d04-204">Esempio</span><span class="sxs-lookup"><span data-stu-id="00d04-204">Examples</span></span>

<span data-ttu-id="00d04-205">La seguente [modifica StartMode di un esempio di servizio](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell, Estratto dalla raccolta TechNet, modifica la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="00d04-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="00d04-206">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d04-206">Requirements</span></span>



| <span data-ttu-id="00d04-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d04-207">Requirement</span></span> | <span data-ttu-id="00d04-208">Valore</span><span class="sxs-lookup"><span data-stu-id="00d04-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00d04-209">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d04-209">Minimum supported client</span></span><br/> | <span data-ttu-id="00d04-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00d04-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00d04-211">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d04-211">Minimum supported server</span></span><br/> | <span data-ttu-id="00d04-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00d04-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00d04-213">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00d04-213">Namespace</span></span><br/>                | <span data-ttu-id="00d04-214">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="00d04-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="00d04-215">MOF</span><span class="sxs-lookup"><span data-stu-id="00d04-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00d04-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00d04-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="00d04-217">DLL</span><span class="sxs-lookup"><span data-stu-id="00d04-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d04-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d04-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d04-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00d04-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="00d04-220">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00d04-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="00d04-221">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="00d04-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="00d04-222">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="00d04-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

