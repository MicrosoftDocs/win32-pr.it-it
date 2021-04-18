---
description: Nell'elenco seguente sono elencati gli eventi supportati dai log WMI in Windows Vista e nei sistemi operativi successivi.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Messaggi di evento WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310339"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="7b8df-103">Messaggi di evento WMI</span><span class="sxs-lookup"><span data-stu-id="7b8df-103">WMI Event Messages</span></span>

<span data-ttu-id="7b8df-104">Nell'elenco seguente sono elencati gli eventi supportati dai log WMI in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="7b8df-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="7b8df-105">La documentazione seguente è progettata per gli sviluppatori e gli amministratori IT.</span><span class="sxs-lookup"><span data-stu-id="7b8df-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="7b8df-106">Se si sta tentando di risolvere un messaggio di errore WMI nel sistema principale, fare riferimento al sito Web [supporto tecnico Microsoft](https://support.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="7b8df-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="7b8df-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_repository WBEM \_ MC \_ incoerente**</span><span class="sxs-lookup"><span data-stu-id="7b8df-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-108">1073747424 (0x400015E0)</span><span class="sxs-lookup"><span data-stu-id="7b8df-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-109">Il servizio Strumentazione gestione Windows ha rilevato un'incoerenza con il repository WMI nel repository di directory *% windir% \\ system32 \\ WBEM \\* e non è stato in grado di recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="7b8df-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="7b8df-110">Il repository WMI verrà ora eliminato. verrà creato un nuovo repository basato sul meccanismo di recupero automatico.</span><span class="sxs-lookup"><span data-stu-id="7b8df-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_caricamento del \_ \_ \_ provider LocalSystem del sottosistema del provider \_ di WBEM MC \_**</span><span class="sxs-lookup"><span data-stu-id="7b8df-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-112">2147483711 (0x8000003F)</span><span class="sxs-lookup"><span data-stu-id="7b8df-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-113">Un provider %1 è stato registrato nello spazio dei nomi Strumentazione gestione Windows %2 per l'utilizzo dell'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="7b8df-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="7b8df-114">Questo account è con privilegi e il provider può causare una violazione della sicurezza se non rappresenta correttamente le richieste degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7b8df-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_MOF MC \_ MOF \_ non \_ caricato \_ al \_ ripristino**</span><span class="sxs-lookup"><span data-stu-id="7b8df-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-116">3221225476 (0xC0000004)</span><span class="sxs-lookup"><span data-stu-id="7b8df-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-117">Si è verificato l'errore %1 durante il tentativo di caricare il file MOF %2 durante il ripristino. File MOF contrassegnato con autocover.</span><span class="sxs-lookup"><span data-stu-id="7b8df-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ non è in grado di \_ attivare il \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="7b8df-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-119">3221225482 (0xC000000A)</span><span class="sxs-lookup"><span data-stu-id="7b8df-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-120">Impossibile riattivare il filtro eventi con query "%2" nello spazio dei nomi "%1" a causa dell'errore %3.</span><span class="sxs-lookup"><span data-stu-id="7b8df-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="7b8df-121">Non è possibile recapitare gli eventi tramite questo filtro fino a quando il problema non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="7b8df-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_query del provider di eventi WBEM MC \_ non valida \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b8df-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-123">3221225493 (0xC0000015)</span><span class="sxs-lookup"><span data-stu-id="7b8df-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-124">Il provider di eventi %1 ha tentato di registrare una query sintatticamente non valida "%2".</span><span class="sxs-lookup"><span data-stu-id="7b8df-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="7b8df-125">La query verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="7b8df-125">The query will be ignored.</span></span> <span data-ttu-id="7b8df-126">È possibile correggere la query esaminando il repository WMI con CIM Studio e aggiornando le sottoscrizioni permanenti per il provider e la query elencati.</span><span class="sxs-lookup"><span data-stu-id="7b8df-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="7b8df-127">Se la sottoscrizione permanente viene creata con un file MOF in arrivo con un prodotto installato, è necessario contattare il fornitore dell'applicazione per correggere la registrazione non funzionante.</span><span class="sxs-lookup"><span data-stu-id="7b8df-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ \_ query intrinseca del provider di eventi WBEM MC non valida \_**</span><span class="sxs-lookup"><span data-stu-id="7b8df-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-129">3221225494 (0xC0000016)</span><span class="sxs-lookup"><span data-stu-id="7b8df-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-130">Il provider di eventi %1 ha tentato di registrare una query di eventi intrinseca "%2" nello spazio dei nomi %3 per il quale non è stato possibile determinare il set di classi di oggetti di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b8df-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="7b8df-131">La query verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="7b8df-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_query del provider di eventi WBEM MC \_ \_ \_ \_ troppo \_ ampia**</span><span class="sxs-lookup"><span data-stu-id="7b8df-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-133">3221225495 (0xC0000017)</span><span class="sxs-lookup"><span data-stu-id="7b8df-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-134">Il provider di eventi %1 ha tentato di registrare la query "%2" nello spazio dei nomi %3 troppo ampio.</span><span class="sxs-lookup"><span data-stu-id="7b8df-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="7b8df-135">I provider di eventi non possono fornire eventi forniti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7b8df-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="7b8df-136">La query verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="7b8df-136">The query will be ignored.</span></span> <span data-ttu-id="7b8df-137">Contattare il fornitore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b8df-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_query del provider di eventi WBEM MC \_ \_ \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="7b8df-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-139">3221225496 (0xC0000018)</span><span class="sxs-lookup"><span data-stu-id="7b8df-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-140">Il provider di eventi %1 ha tentato di registrare la query "%2" la cui classe di destinazione "%3" nello spazio dei nomi %4 non esiste.</span><span class="sxs-lookup"><span data-stu-id="7b8df-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="7b8df-141">La query verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="7b8df-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_evento di \_ query del provider di eventi WBEM MC \_ \_ \_ non \_**</span><span class="sxs-lookup"><span data-stu-id="7b8df-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-143">3221225497 (0xC0000019)</span><span class="sxs-lookup"><span data-stu-id="7b8df-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-144">Il provider di eventi %1 ha tentato di registrare &quot; la query %2 &quot; la cui classe &quot; di destinazione %3 &quot; non è una classe di evento.</span><span class="sxs-lookup"><span data-stu-id="7b8df-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="7b8df-145">La query verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="7b8df-145">The query will be ignored.</span></span> <span data-ttu-id="7b8df-146">Contattare il fornitore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b8df-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**\_errore di \_ \_ Core WBEM MC WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="7b8df-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-148">3221225500 (0xC000001C)</span><span class="sxs-lookup"><span data-stu-id="7b8df-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-149">Non è stato possibile inizializzare il sottosistema o il sottosistema WMI o il sottosistema di eventi con numero di errore %1.</span><span class="sxs-lookup"><span data-stu-id="7b8df-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="7b8df-150">Il problema potrebbe essere dovuto a una versione non installata di WMI, a un errore di aggiornamento del repository WMI, a spazio su disco insufficiente o a memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7b8df-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_errore di connessione WBEM MC \_ ADAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b8df-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-152">3221225515 (0xC000002B)</span><span class="sxs-lookup"><span data-stu-id="7b8df-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-153">Strumentazione gestione Windows ADAP non è riuscito a connettersi allo spazio dei nomi %1 con l'errore seguente %2.</span><span class="sxs-lookup"><span data-stu-id="7b8df-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**\_ \_ \_ \_ errore Perflib PUTCLASS \_ di WBEM MC ADAP**</span><span class="sxs-lookup"><span data-stu-id="7b8df-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-155">3221225520 (0xC0000030)</span><span class="sxs-lookup"><span data-stu-id="7b8df-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-156">Strumentazione gestione Windows ADAP non è stato in grado di salvare l'oggetto %1 nello spazio dei nomi %2 a causa del seguente errore %3.</span><span class="sxs-lookup"><span data-stu-id="7b8df-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ non è \_ in grado di \_ aggiungere \_ WIN32PERF**</span><span class="sxs-lookup"><span data-stu-id="7b8df-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-158">3221225530 (0xC000003A)</span><span class="sxs-lookup"><span data-stu-id="7b8df-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-159">Strumentazione gestione Windows ADAP non è stato in grado di creare la \_ classe base delle prestazioni Win32 in %1: risultato = %2.</span><span class="sxs-lookup"><span data-stu-id="7b8df-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ non è \_ in grado di \_ aggiungere \_ WIN32PERFRAWDATA**</span><span class="sxs-lookup"><span data-stu-id="7b8df-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-161">3221225531 (0xC000003B)</span><span class="sxs-lookup"><span data-stu-id="7b8df-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-162">Strumentazione gestione Windows ADAP non è stato in grado di creare la \_ classe di base Win32 PerfRawData %1.</span><span class="sxs-lookup"><span data-stu-id="7b8df-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ non è stato \_ possibile \_ avviare il repository WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="7b8df-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-164">3221231073 (0xC00015E1)</span><span class="sxs-lookup"><span data-stu-id="7b8df-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-165">Il servizio Strumentazione gestione Windows non è riuscito a caricare i file del repository nel repository di directory *% windir% \\ system32 \\ WBEM \\*.</span><span class="sxs-lookup"><span data-stu-id="7b8df-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="7b8df-166">Questo problema può essere causato da un danneggiamento nei file del repository, dalle impostazioni di sicurezza di questa directory, dalla mancanza di spazio su disco o da altri problemi di risorse di sistema, ad esempio la mancanza di memoria.</span><span class="sxs-lookup"><span data-stu-id="7b8df-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="7b8df-167">Se questo errore si verifica ogni volta che il computer viene riavviato, l'amministratore di questo computer potrebbe dover arrestare il servizio WMI, verificare l'impostazione di sicurezza sulla cartella e i file in questa cartella ed eseguire WMIDiag per convalidare l'integrità del Strumentazione gestione Windows.</span><span class="sxs-lookup"><span data-stu-id="7b8df-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ richiede la \_ crittografia \_ negata**</span><span class="sxs-lookup"><span data-stu-id="7b8df-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-169">3221231077 (0xC00015E5)</span><span class="sxs-lookup"><span data-stu-id="7b8df-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-170">Accesso allo spazio dei nomi %1 negato perché lo spazio dei nomi è contrassegnato con RequiresEncryption, ma lo script o l'applicazione ha tentato di connettersi a questo spazio dei nomi con un livello di autenticazione inferiore alla **\_ privacy di PKT**.</span><span class="sxs-lookup"><span data-stu-id="7b8df-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="7b8df-171">Modificare il livello di autenticazione in **PKT \_ privacy** , quindi eseguire di nuovo lo script o l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b8df-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ richiede la \_ crittografia \_ asincrona \_ negata**</span><span class="sxs-lookup"><span data-stu-id="7b8df-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-173">3221231078 (0xC00015E6)</span><span class="sxs-lookup"><span data-stu-id="7b8df-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-174">Impossibile recapitare i risultati in modo asincrono per lo spazio dei nomi %1. Strumentazione gestione Windows</span><span class="sxs-lookup"><span data-stu-id="7b8df-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="7b8df-175">Lo spazio dei nomi è contrassegnato con RequiresEncryption, ma WinMgmt non è riuscito a stabilire una connessione sicura al computer client.</span><span class="sxs-lookup"><span data-stu-id="7b8df-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="7b8df-176">Verificare che sia presente una relazione di trust tra i computer client e server in modo che il client riconosca l'account del computer server.</span><span class="sxs-lookup"><span data-stu-id="7b8df-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**l' \_ \_ host WBEM MC WBEM è stato \_ \_ ucciso**</span><span class="sxs-lookup"><span data-stu-id="7b8df-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-178">3221231084 (0xC00015EC)</span><span class="sxs-lookup"><span data-stu-id="7b8df-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-179">Il Strumentazione gestione Windows è stato interrotto WMIPRVSE.EXE perché una quota ha raggiunto un valore di avviso.</span><span class="sxs-lookup"><span data-stu-id="7b8df-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="7b8df-180">Quota: %1 valore: %2 valore massimo: %3 WMIPRVSE PID: %4.</span><span class="sxs-lookup"><span data-stu-id="7b8df-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="7b8df-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-182">3221231086 (0xC00015EE)</span><span class="sxs-lookup"><span data-stu-id="7b8df-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-183">Durante l'avvio del servizio, il servizio Strumentazione gestione Windows non è stato in grado di individuare i file del repository.</span><span class="sxs-lookup"><span data-stu-id="7b8df-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="7b8df-184">Verrà creato un nuovo repository basato sul meccanismo di recupero automatico.</span><span class="sxs-lookup"><span data-stu-id="7b8df-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ ha avviato \_ è stata**</span><span class="sxs-lookup"><span data-stu-id="7b8df-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-186">3221231087 (0xC00015EF)</span><span class="sxs-lookup"><span data-stu-id="7b8df-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-187">Il servizio Strumentazione gestione Windows è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="7b8df-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**si \_ è \_ \_ \_ \_ inizializzato l'ESS \_ di WBEM MC WBEM Core PSS**</span><span class="sxs-lookup"><span data-stu-id="7b8df-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-189">3221231089 (0xC00015F1)</span><span class="sxs-lookup"><span data-stu-id="7b8df-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-190">Strumentazione gestione Windows sottosistemi di servizio inizializzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="7b8df-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_errore di \_ \_ \_ inizializzazione del \_ servizio WBEM MC WBEM**</span><span class="sxs-lookup"><span data-stu-id="7b8df-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-192">3221225501 (0xC000001D)</span><span class="sxs-lookup"><span data-stu-id="7b8df-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-193">Il numero di errore %1 è stato restituito durante il tentativo di inizializzare Strumentazione gestione Windows servizio.</span><span class="sxs-lookup"><span data-stu-id="7b8df-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="7b8df-194">Il problema potrebbe essere dovuto a una versione non installata di WMI, a un errore di aggiornamento del repository WMI, a spazio su disco insufficiente o a memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7b8df-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b8df-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**\_repository WBEM \_ MC \_ WBEM \_ ricreato**</span><span class="sxs-lookup"><span data-stu-id="7b8df-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b8df-196">3221231088 (0xC00015F0)</span><span class="sxs-lookup"><span data-stu-id="7b8df-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="7b8df-197">Strumentazione gestione Windows repository è stato ricreato con il meccanismo di recupero automatico.</span><span class="sxs-lookup"><span data-stu-id="7b8df-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b8df-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b8df-198">Requirements</span></span>



| <span data-ttu-id="7b8df-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b8df-199">Requirement</span></span> | <span data-ttu-id="7b8df-200">Valore</span><span class="sxs-lookup"><span data-stu-id="7b8df-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7b8df-201">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b8df-201">Minimum supported client</span></span><br/> | <span data-ttu-id="7b8df-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b8df-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7b8df-203">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b8df-203">Minimum supported server</span></span><br/> | <span data-ttu-id="7b8df-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b8df-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b8df-205">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b8df-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b8df-206">Eventi WMI</span><span class="sxs-lookup"><span data-stu-id="7b8df-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

[<span data-ttu-id="7b8df-207">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="7b8df-207">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> </dl>

 

 




