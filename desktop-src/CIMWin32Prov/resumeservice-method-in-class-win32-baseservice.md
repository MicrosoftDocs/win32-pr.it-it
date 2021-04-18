---
description: Esegue un tentativo di ripresa del servizio.
ms.assetid: df582402-d932-4132-a1ad-257b2993bbf6
ms.tgt_platform: multiple
title: Metodo ResumeService della classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bba09180121d5649542f70a01adf2cb3acd7b142
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304576"
---
# <a name="resumeservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="c8b57-103">Metodo ResumeService della \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="c8b57-103">ResumeService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="c8b57-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta di collocare il servizio nello stato resumed.</span><span class="sxs-lookup"><span data-stu-id="c8b57-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the resumed state.</span></span>

<span data-ttu-id="c8b57-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c8b57-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c8b57-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c8b57-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b57-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8b57-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="c8b57-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8b57-108">Parameters</span></span>

<span data-ttu-id="c8b57-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c8b57-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8b57-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8b57-110">Return value</span></span>

<span data-ttu-id="c8b57-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c8b57-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c8b57-112">**Success**</span><span class="sxs-lookup"><span data-stu-id="c8b57-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-113">0</span><span class="sxs-lookup"><span data-stu-id="c8b57-113">0</span></span>

<span data-ttu-id="c8b57-114">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="c8b57-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-115">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="c8b57-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-116">1</span><span class="sxs-lookup"><span data-stu-id="c8b57-116">1</span></span>

<span data-ttu-id="c8b57-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="c8b57-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-118">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="c8b57-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-119">2</span><span class="sxs-lookup"><span data-stu-id="c8b57-119">2</span></span>

<span data-ttu-id="c8b57-120">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="c8b57-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-121">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="c8b57-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-122">3</span><span class="sxs-lookup"><span data-stu-id="c8b57-122">3</span></span>

<span data-ttu-id="c8b57-123">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-124">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="c8b57-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-125">4</span><span class="sxs-lookup"><span data-stu-id="c8b57-125">4</span></span>

<span data-ttu-id="c8b57-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-127">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="c8b57-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-128">5</span><span class="sxs-lookup"><span data-stu-id="c8b57-128">5</span></span>

<span data-ttu-id="c8b57-129">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio (proprietà di [**stato**](win32-baseservice.md) [**\_ BaseService Win32**](win32-baseservice.md)) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c8b57-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-130">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="c8b57-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-131">6</span><span class="sxs-lookup"><span data-stu-id="c8b57-131">6</span></span>

<span data-ttu-id="c8b57-132">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="c8b57-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-133">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="c8b57-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-134">7</span><span class="sxs-lookup"><span data-stu-id="c8b57-134">7</span></span>

<span data-ttu-id="c8b57-135">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-136">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="c8b57-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-137">8</span><span class="sxs-lookup"><span data-stu-id="c8b57-137">8</span></span>

<span data-ttu-id="c8b57-138">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="c8b57-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-139">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="c8b57-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-140">9</span><span class="sxs-lookup"><span data-stu-id="c8b57-140">9</span></span>

<span data-ttu-id="c8b57-141">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-142">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="c8b57-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-143">10</span><span class="sxs-lookup"><span data-stu-id="c8b57-143">10</span></span>

<span data-ttu-id="c8b57-144">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c8b57-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-145">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="c8b57-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-146">11</span><span class="sxs-lookup"><span data-stu-id="c8b57-146">11</span></span>

<span data-ttu-id="c8b57-147">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="c8b57-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-148">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="c8b57-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-149">12</span><span class="sxs-lookup"><span data-stu-id="c8b57-149">12</span></span>

<span data-ttu-id="c8b57-150">Il servizio si basa su una dipendenza che è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b57-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-151">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="c8b57-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-152">13</span><span class="sxs-lookup"><span data-stu-id="c8b57-152">13</span></span>

<span data-ttu-id="c8b57-153">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="c8b57-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-154">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="c8b57-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-155">14</span><span class="sxs-lookup"><span data-stu-id="c8b57-155">14</span></span>

<span data-ttu-id="c8b57-156">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b57-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-157">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="c8b57-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-158">15</span><span class="sxs-lookup"><span data-stu-id="c8b57-158">15</span></span>

<span data-ttu-id="c8b57-159">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b57-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-160">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="c8b57-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-161">16</span><span class="sxs-lookup"><span data-stu-id="c8b57-161">16</span></span>

<span data-ttu-id="c8b57-162">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b57-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-163">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="c8b57-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-164">17</span><span class="sxs-lookup"><span data-stu-id="c8b57-164">17</span></span>

<span data-ttu-id="c8b57-165">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-166">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="c8b57-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-167">18</span><span class="sxs-lookup"><span data-stu-id="c8b57-167">18</span></span>

<span data-ttu-id="c8b57-168">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="c8b57-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-169">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="c8b57-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-170">19</span><span class="sxs-lookup"><span data-stu-id="c8b57-170">19</span></span>

<span data-ttu-id="c8b57-171">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="c8b57-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-172">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="c8b57-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-173">20</span><span class="sxs-lookup"><span data-stu-id="c8b57-173">20</span></span>

<span data-ttu-id="c8b57-174">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="c8b57-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-175">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="c8b57-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-176">21</span><span class="sxs-lookup"><span data-stu-id="c8b57-176">21</span></span>

<span data-ttu-id="c8b57-177">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-178">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="c8b57-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-179">22</span><span class="sxs-lookup"><span data-stu-id="c8b57-179">22</span></span>

<span data-ttu-id="c8b57-180">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="c8b57-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-181">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="c8b57-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-182">23</span><span class="sxs-lookup"><span data-stu-id="c8b57-182">23</span></span>

<span data-ttu-id="c8b57-183">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b57-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-184">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="c8b57-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-185">24</span><span class="sxs-lookup"><span data-stu-id="c8b57-185">24</span></span>

<span data-ttu-id="c8b57-186">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c8b57-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c8b57-187">**Altri**</span><span class="sxs-lookup"><span data-stu-id="c8b57-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c8b57-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c8b57-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8b57-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8b57-189">Requirements</span></span>



| <span data-ttu-id="c8b57-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b57-190">Requirement</span></span> | <span data-ttu-id="c8b57-191">Valore</span><span class="sxs-lookup"><span data-stu-id="c8b57-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b57-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8b57-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b57-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8b57-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8b57-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8b57-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b57-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8b57-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8b57-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c8b57-196">Namespace</span></span><br/>                | <span data-ttu-id="c8b57-197">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c8b57-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8b57-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c8b57-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8b57-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8b57-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8b57-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c8b57-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8b57-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8b57-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b57-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8b57-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8b57-203">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8b57-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c8b57-204">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="c8b57-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

