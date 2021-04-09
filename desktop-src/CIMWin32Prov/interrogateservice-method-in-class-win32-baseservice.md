---
description: Richiede che il servizio aggiorni lo stato a Service Manager.
ms.assetid: 118156ef-ee43-4f73-af41-e295a0a850b9
ms.tgt_platform: multiple
title: Metodo InterrogateService della classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29e29c152e7fea8de7a2ccaf1e7d86bf3a08d4c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966058"
---
# <a name="interrogateservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="9a24e-103">Metodo InterrogateService della \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="9a24e-103">InterrogateService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="9a24e-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** richiede che il servizio aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="9a24e-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the service update its state to the service manager.</span></span>

<span data-ttu-id="9a24e-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9a24e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9a24e-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9a24e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a24e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a24e-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="9a24e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a24e-108">Parameters</span></span>

<span data-ttu-id="9a24e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9a24e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a24e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a24e-110">Return value</span></span>

<span data-ttu-id="9a24e-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="9a24e-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9a24e-112">**Success**</span><span class="sxs-lookup"><span data-stu-id="9a24e-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-113">0</span><span class="sxs-lookup"><span data-stu-id="9a24e-113">0</span></span>

<span data-ttu-id="9a24e-114">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="9a24e-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-115">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="9a24e-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-116">1</span><span class="sxs-lookup"><span data-stu-id="9a24e-116">1</span></span>

<span data-ttu-id="9a24e-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9a24e-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-118">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="9a24e-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-119">2</span><span class="sxs-lookup"><span data-stu-id="9a24e-119">2</span></span>

<span data-ttu-id="9a24e-120">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="9a24e-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-121">**Servizi dipendenti in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="9a24e-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-122">3</span><span class="sxs-lookup"><span data-stu-id="9a24e-122">3</span></span>

<span data-ttu-id="9a24e-123">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-124">**Controllo del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="9a24e-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-125">4</span><span class="sxs-lookup"><span data-stu-id="9a24e-125">4</span></span>

<span data-ttu-id="9a24e-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-127">**Il servizio non può accettare il controllo**</span><span class="sxs-lookup"><span data-stu-id="9a24e-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-128">5</span><span class="sxs-lookup"><span data-stu-id="9a24e-128">5</span></span>

<span data-ttu-id="9a24e-129">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio (proprietà di [**stato**](win32-baseservice.md) [**\_ BaseService Win32**](win32-baseservice.md)) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="9a24e-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-130">**Servizio non attivo**</span><span class="sxs-lookup"><span data-stu-id="9a24e-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-131">6</span><span class="sxs-lookup"><span data-stu-id="9a24e-131">6</span></span>

<span data-ttu-id="9a24e-132">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="9a24e-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-133">**Timeout richiesta servizio**</span><span class="sxs-lookup"><span data-stu-id="9a24e-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-134">7</span><span class="sxs-lookup"><span data-stu-id="9a24e-134">7</span></span>

<span data-ttu-id="9a24e-135">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-136">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="9a24e-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-137">8</span><span class="sxs-lookup"><span data-stu-id="9a24e-137">8</span></span>

<span data-ttu-id="9a24e-138">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="9a24e-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-139">**Percorso non trovato**</span><span class="sxs-lookup"><span data-stu-id="9a24e-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-140">9</span><span class="sxs-lookup"><span data-stu-id="9a24e-140">9</span></span>

<span data-ttu-id="9a24e-141">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-142">**Servizio già in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="9a24e-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-143">10</span><span class="sxs-lookup"><span data-stu-id="9a24e-143">10</span></span>

<span data-ttu-id="9a24e-144">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a24e-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-145">**Database del servizio bloccato**</span><span class="sxs-lookup"><span data-stu-id="9a24e-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-146">11</span><span class="sxs-lookup"><span data-stu-id="9a24e-146">11</span></span>

<span data-ttu-id="9a24e-147">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="9a24e-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-148">**Dipendenza servizio eliminata**</span><span class="sxs-lookup"><span data-stu-id="9a24e-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-149">12</span><span class="sxs-lookup"><span data-stu-id="9a24e-149">12</span></span>

<span data-ttu-id="9a24e-150">Il servizio si basa su una dipendenza che è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9a24e-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-151">**Errore di dipendenza del servizio**</span><span class="sxs-lookup"><span data-stu-id="9a24e-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-152">13</span><span class="sxs-lookup"><span data-stu-id="9a24e-152">13</span></span>

<span data-ttu-id="9a24e-153">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="9a24e-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-154">**Servizio disabilitato**</span><span class="sxs-lookup"><span data-stu-id="9a24e-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-155">14</span><span class="sxs-lookup"><span data-stu-id="9a24e-155">14</span></span>

<span data-ttu-id="9a24e-156">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9a24e-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-157">**Accesso al servizio non riuscito**</span><span class="sxs-lookup"><span data-stu-id="9a24e-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-158">15</span><span class="sxs-lookup"><span data-stu-id="9a24e-158">15</span></span>

<span data-ttu-id="9a24e-159">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9a24e-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-160">**Servizio contrassegnato per l'eliminazione**</span><span class="sxs-lookup"><span data-stu-id="9a24e-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-161">16</span><span class="sxs-lookup"><span data-stu-id="9a24e-161">16</span></span>

<span data-ttu-id="9a24e-162">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9a24e-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-163">**Servizio senza thread**</span><span class="sxs-lookup"><span data-stu-id="9a24e-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-164">17</span><span class="sxs-lookup"><span data-stu-id="9a24e-164">17</span></span>

<span data-ttu-id="9a24e-165">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-166">**Stato dipendenza circolare**</span><span class="sxs-lookup"><span data-stu-id="9a24e-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-167">18</span><span class="sxs-lookup"><span data-stu-id="9a24e-167">18</span></span>

<span data-ttu-id="9a24e-168">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="9a24e-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-169">**Stato nome duplicato**</span><span class="sxs-lookup"><span data-stu-id="9a24e-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-170">19</span><span class="sxs-lookup"><span data-stu-id="9a24e-170">19</span></span>

<span data-ttu-id="9a24e-171">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="9a24e-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-172">**Stato nome non valido**</span><span class="sxs-lookup"><span data-stu-id="9a24e-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-173">20</span><span class="sxs-lookup"><span data-stu-id="9a24e-173">20</span></span>

<span data-ttu-id="9a24e-174">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="9a24e-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-175">**Stato parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="9a24e-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-176">21</span><span class="sxs-lookup"><span data-stu-id="9a24e-176">21</span></span>

<span data-ttu-id="9a24e-177">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-178">**Stato account del servizio non valido**</span><span class="sxs-lookup"><span data-stu-id="9a24e-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-179">22</span><span class="sxs-lookup"><span data-stu-id="9a24e-179">22</span></span>

<span data-ttu-id="9a24e-180">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="9a24e-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-181">**Il servizio stato esiste**</span><span class="sxs-lookup"><span data-stu-id="9a24e-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-182">23</span><span class="sxs-lookup"><span data-stu-id="9a24e-182">23</span></span>

<span data-ttu-id="9a24e-183">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9a24e-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-184">**Servizio già sospeso**</span><span class="sxs-lookup"><span data-stu-id="9a24e-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-185">24</span><span class="sxs-lookup"><span data-stu-id="9a24e-185">24</span></span>

<span data-ttu-id="9a24e-186">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9a24e-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a24e-187">**Altri**</span><span class="sxs-lookup"><span data-stu-id="9a24e-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9a24e-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="9a24e-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a24e-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a24e-189">Requirements</span></span>



| <span data-ttu-id="9a24e-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a24e-190">Requirement</span></span> | <span data-ttu-id="9a24e-191">Valore</span><span class="sxs-lookup"><span data-stu-id="9a24e-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a24e-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a24e-192">Minimum supported client</span></span><br/> | <span data-ttu-id="9a24e-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a24e-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a24e-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a24e-194">Minimum supported server</span></span><br/> | <span data-ttu-id="9a24e-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a24e-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a24e-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a24e-196">Namespace</span></span><br/>                | <span data-ttu-id="9a24e-197">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9a24e-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a24e-198">MOF</span><span class="sxs-lookup"><span data-stu-id="9a24e-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a24e-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a24e-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a24e-200">DLL</span><span class="sxs-lookup"><span data-stu-id="9a24e-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a24e-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a24e-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a24e-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a24e-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a24e-203">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a24e-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9a24e-204">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="9a24e-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

