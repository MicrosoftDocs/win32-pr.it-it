---
description: Se si verifica un errore, WMI restituisce un codice di errore come valore HRESULT. Questi codici possono essere restituiti da script, applicazioni C++ o WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Costanti di errore WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309754"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="e419e-104">Costanti di errore WMI</span><span class="sxs-lookup"><span data-stu-id="e419e-104">WMI Error Constants</span></span>

<span data-ttu-id="e419e-105">Se si verifica un errore, WMI restituisce un codice di errore come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e419e-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="e419e-106">Questi codici possono essere restituiti da script, applicazioni C++ o [**wmic**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="e419e-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="e419e-107">La seguente documentazione è destinata agli sviluppatori e agli amministratori IT.</span><span class="sxs-lookup"><span data-stu-id="e419e-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="e419e-108">Se si è un utente finale che ha riscontrato un messaggio di errore relativo a WMI, è necessario passare a [supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="e419e-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="e419e-109">Per ulteriori informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere [WMI non funziona](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="e419e-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="e419e-110">Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="e419e-111">Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="e419e-112">In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.</span><span class="sxs-lookup"><span data-stu-id="e419e-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="e419e-113">Per ottenere ulteriori informazioni sull'origine del problema, è possibile scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e419e-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="e419e-114">Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo.</span><span class="sxs-lookup"><span data-stu-id="e419e-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="e419e-115">Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e419e-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="e419e-116">È possibile scaricare il Utilità di diagnosi di WMI [qui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="e419e-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="e419e-117">Alcuni metodi delle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio, 64).</span><span class="sxs-lookup"><span data-stu-id="e419e-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="e419e-118">È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="e419e-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="e419e-119">Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e419e-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="e419e-120">Nell'elenco seguente sono elencati alcuni intervalli comuni di errori.</span><span class="sxs-lookup"><span data-stu-id="e419e-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="e419e-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span><span class="sxs-lookup"><span data-stu-id="e419e-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="e419e-122">Errori che hanno origine in WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="e419e-123">Un'operazione WMI specifica non è riuscita a causa di</span><span class="sxs-lookup"><span data-stu-id="e419e-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="e419e-124">Un errore nella richiesta, ad esempio, una query WQL ha esito negativo o l'account non dispone delle autorizzazioni corrette.</span><span class="sxs-lookup"><span data-stu-id="e419e-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="e419e-125">Un problema di infrastruttura WMI, ad esempio la registrazione CIM o DCOM non corretta.</span><span class="sxs-lookup"><span data-stu-id="e419e-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="e419e-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="e419e-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="e419e-127">Errori originati nel sistema operativo di base.</span><span class="sxs-lookup"><span data-stu-id="e419e-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="e419e-128">WMI può restituire questo tipo di errore a causa di un errore esterno, ad esempio un errore di sicurezza DCOM.</span><span class="sxs-lookup"><span data-stu-id="e419e-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="e419e-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="e419e-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="e419e-130">Errori provenienti da DCOM.</span><span class="sxs-lookup"><span data-stu-id="e419e-130">Errors originating in DCOM.</span></span> <span data-ttu-id="e419e-131">La configurazione DCOM per le operazioni in un computer remoto, ad esempio, potrebbe non essere corretta.</span><span class="sxs-lookup"><span data-stu-id="e419e-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="e419e-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="e419e-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="e419e-133">Errore originato da ADSI (Active Directory interfacce del servizio) o LDAP (Lightweight Directory Access Protocol), ad esempio, un errore di accesso Active Directory quando si utilizzano i provider di Active Directory WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="e419e-134">Alcuni metodi delle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio, 64).</span><span class="sxs-lookup"><span data-stu-id="e419e-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="e419e-135">È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="e419e-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="e419e-136">Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e419e-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="e419e-137">In C++ è possibile chiamare [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e specificare **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** come modulo Message.</span><span class="sxs-lookup"><span data-stu-id="e419e-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="e419e-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="e419e-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-139">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e419e-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-140">Chiamata non riuscita.</span><span class="sxs-lookup"><span data-stu-id="e419e-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e419e-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-142">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="e419e-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-143">Impossibile trovare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e419e-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**accesso a WBEM \_ E \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="e419e-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-145">2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="e419e-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-146">L'utente corrente non dispone delle autorizzazioni necessarie per eseguire l'azione.</span><span class="sxs-lookup"><span data-stu-id="e419e-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_errore del \_ provider WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-148">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="e419e-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-149">Il provider ha avuto esito negativo in un momento diverso dall'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="e419e-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_tipo WBEM E non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="e419e-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-151">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="e419e-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-152">Mancata corrispondenza del tipo.</span><span class="sxs-lookup"><span data-stu-id="e419e-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ \_ \_ memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="e419e-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-154">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="e419e-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-155">Memoria insufficiente per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e419e-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_contesto WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-157">2147749895 (0x80041007)</span><span class="sxs-lookup"><span data-stu-id="e419e-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-158">L'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) non è valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_parametro WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-160">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e419e-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-161">Uno dei parametri della chiamata non è corretto.</span><span class="sxs-lookup"><span data-stu-id="e419e-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="e419e-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-163">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="e419e-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-164">La risorsa, in genere un server remoto, non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="e419e-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM \_ E \_ \_ errore critico**</span><span class="sxs-lookup"><span data-stu-id="e419e-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-166">2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="e419e-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-167">Si è verificato un errore interno, critico e imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e419e-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="e419e-168">Segnalare l'errore al supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e419e-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_flusso WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-170">2147749899 (0x8004100B)</span><span class="sxs-lookup"><span data-stu-id="e419e-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-171">Nel corso di una sessione remota uno o più pacchetti di rete erano danneggiati.</span><span class="sxs-lookup"><span data-stu-id="e419e-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e419e-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-173">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="e419e-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-174">Funzionalità o operazione non supportata.</span><span class="sxs-lookup"><span data-stu-id="e419e-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**superclasse WBEM \_ E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-176">2147749901 (0x8004100D)</span><span class="sxs-lookup"><span data-stu-id="e419e-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-177">Classe padre specificata non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**\_ \_ spazio dei nomi WBEM E non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-179">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="e419e-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-180">Impossibile trovare lo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="e419e-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_oggetto WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-182">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="e419e-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-183">L'istanza specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_classe WBEM \_ E \_ classe non valida**</span><span class="sxs-lookup"><span data-stu-id="e419e-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-185">2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="e419e-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-186">La classe specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_provider WBEM \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e419e-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-188">2147749905 (0x80041011)</span><span class="sxs-lookup"><span data-stu-id="e419e-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-189">Il provider a cui viene fatto riferimento nello schema non dispone di una registrazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e419e-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_registrazione del provider WBEM E \_ non valida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="e419e-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="e419e-192">Il provider a cui viene fatto riferimento nello schema ha una registrazione errata o incompleta.</span><span class="sxs-lookup"><span data-stu-id="e419e-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="e419e-193">Questo errore può essere causato da molte condizioni, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="e419e-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="e419e-194">Comando per [ \# lo spazio dei nomi pragma](pragma-namespace.md) mancante nel file Managed Object Format (MOF) usato per registrare il provider.</span><span class="sxs-lookup"><span data-stu-id="e419e-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="e419e-195">Il provider può essere registrato nello spazio dei nomi WMI errato.</span><span class="sxs-lookup"><span data-stu-id="e419e-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="e419e-196">Errore durante il recupero della registrazione COM.</span><span class="sxs-lookup"><span data-stu-id="e419e-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="e419e-197">Il modello di hosting non è valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-197">Hosting model is not valid.</span></span> <span data-ttu-id="e419e-198">Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="e419e-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="e419e-199">Una classe specificata nella registrazione non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="e419e-200">Impossibile creare un'istanza di o ereditare dalla classe [**\_ \_ Win32Provider**](--win32provider.md) per creare la registrazione del provider nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="e419e-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_errore di \_ caricamento del provider WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-202">2147749907 (0x80041013)</span><span class="sxs-lookup"><span data-stu-id="e419e-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-203">COM non può individuare un provider cui si fa riferimento nello schema.</span><span class="sxs-lookup"><span data-stu-id="e419e-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="e419e-204">Questo errore può essere causato da molte condizioni, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="e419e-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="e419e-205">Il provider utilizza una DLL WMI che non corrisponde al file con estensione lib utilizzato al momento della compilazione del provider.</span><span class="sxs-lookup"><span data-stu-id="e419e-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="e419e-206">La DLL del provider, o una qualsiasi DLL da cui dipende, è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="e419e-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="e419e-207">Il provider non è riuscito a esportare [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="e419e-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="e419e-208">Il provider in-process non è stato registrato con il comando **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="e419e-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="e419e-209">Il provider out-of-process non è stato registrato con l'opzione **/regserver** .</span><span class="sxs-lookup"><span data-stu-id="e419e-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="e419e-210">Ad esempio, **myprog.exe/regserver**.</span><span class="sxs-lookup"><span data-stu-id="e419e-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_errore di \_ inizializzazione WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-212">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="e419e-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-213">Impossibile inizializzare il componente, ad esempio un provider, per motivi interni.</span><span class="sxs-lookup"><span data-stu-id="e419e-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_errore di \_ trasporto WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-215">2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="e419e-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-216">Si è verificato un errore di rete che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="e419e-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_operazione WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-218">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="e419e-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-219">L'operazione richiesta non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-219">Requested operation is not valid.</span></span> <span data-ttu-id="e419e-220">Questo errore si applica generalmente a tentativi non validi di eliminare classi o proprietà.</span><span class="sxs-lookup"><span data-stu-id="e419e-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_query WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-222">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="e419e-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-223">La sintassi della query non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo di query WBEM E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-225">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="e419e-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-226">Il linguaggio di query richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e419e-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="e419e-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-228">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="e419e-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-229">In un'operazione Put è stato specificato il flag **wbemChangeFlagCreateOnly** , ma l'istanza esiste già.</span><span class="sxs-lookup"><span data-stu-id="e419e-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**\_sostituzione WBEM \_ E \_ non \_ consentita**</span><span class="sxs-lookup"><span data-stu-id="e419e-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-231">2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="e419e-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-232">Non è possibile eseguire l'operazione di aggiunta su questo qualificatore perché l'oggetto proprietario non consente le sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="e419e-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ qualificatore WBEM E propagato \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-234">2147749915 (0x8004101B)</span><span class="sxs-lookup"><span data-stu-id="e419e-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-235">L'utente ha tentato di eliminare un qualificatore non di proprietà.</span><span class="sxs-lookup"><span data-stu-id="e419e-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="e419e-236">Il qualificatore è stato ereditato da una classe padre.</span><span class="sxs-lookup"><span data-stu-id="e419e-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_Proprietà WBEM E \_ propagata \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-238">2147749916 (0x8004101C)</span><span class="sxs-lookup"><span data-stu-id="e419e-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-239">L'utente ha tentato di eliminare una proprietà che non possedeva.</span><span class="sxs-lookup"><span data-stu-id="e419e-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="e419e-240">La proprietà è stata ereditata da una classe padre.</span><span class="sxs-lookup"><span data-stu-id="e419e-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ imprevisto**</span><span class="sxs-lookup"><span data-stu-id="e419e-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-242">2147749917 (0x8004101D)</span><span class="sxs-lookup"><span data-stu-id="e419e-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-243">Il client ha eseguito una sequenza di chiamate imprevista e non valida, ad esempio la chiamata di [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) prima della chiamata a [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span><span class="sxs-lookup"><span data-stu-id="e419e-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_operazione WBEM E non \_ valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-245">2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="e419e-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-246">L'utente ha richiesto un'operazione non valida, ad esempio la generazione di una classe da un'istanza.</span><span class="sxs-lookup"><span data-stu-id="e419e-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ non può \_ essere una \_ chiave**</span><span class="sxs-lookup"><span data-stu-id="e419e-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-248">2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="e419e-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-249">Tentativo non valido di specificare un qualificatore di chiave su una proprietà che non può essere una chiave.</span><span class="sxs-lookup"><span data-stu-id="e419e-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="e419e-250">Le chiavi sono specificate nella definizione della classe per un oggetto e non possono essere alterate per singole istanze.</span><span class="sxs-lookup"><span data-stu-id="e419e-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_classe WBEM E \_ incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-252">2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="e419e-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-253">L'oggetto corrente non è una definizione di classe valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="e419e-254">Il valore è incompleto o non è stato registrato con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="e419e-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_sintassi WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-256">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="e419e-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-257">La sintassi della query non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM \_ E \_ oggetto non decorato \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-259">2147749922 (0x80041022)</span><span class="sxs-lookup"><span data-stu-id="e419e-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-260">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="e419e-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ sola lettura \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-262">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="e419e-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-263">È stato effettuato un tentativo di modificare una proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e419e-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**il \_ provider WBEM E \_ \_ non è \_ in grado di supportare**</span><span class="sxs-lookup"><span data-stu-id="e419e-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-265">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="e419e-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-266">Il provider non è in grado di eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="e419e-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="e419e-267">Questo può includere una query troppo complessa, il recupero di un'istanza, la creazione o l'aggiornamento di una classe, l'eliminazione di una classe o l'enumerazione di una classe.</span><span class="sxs-lookup"><span data-stu-id="e419e-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E \_ classe \_ con \_ elementi figlio**</span><span class="sxs-lookup"><span data-stu-id="e419e-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-269">2147749925 (0x80041025)</span><span class="sxs-lookup"><span data-stu-id="e419e-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-270">È stato effettuato un tentativo di apportare una modifica che invalida una sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e419e-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**\_classe WBEM \_ E \_ con \_ istanze**</span><span class="sxs-lookup"><span data-stu-id="e419e-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-272">2147749926 (0x80041026)</span><span class="sxs-lookup"><span data-stu-id="e419e-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-273">È stato effettuato un tentativo di eliminare o modificare una classe con istanze.</span><span class="sxs-lookup"><span data-stu-id="e419e-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_query WBEM \_ E \_ non \_ implementata**</span><span class="sxs-lookup"><span data-stu-id="e419e-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-275">2147749927 (0x80041027)</span><span class="sxs-lookup"><span data-stu-id="e419e-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-276">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="e419e-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-278">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="e419e-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-279">Il valore Nothing/**null** è stato specificato per una proprietà che deve avere un valore, ad esempio uno contrassegnato da un qualificatore di [**chiave**](key-qualifier.md), [**indicizzato**](optional-qualifiers.md)o **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="e419e-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_tipo di \_ \_ qualificatore WBEM E non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-281">2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="e419e-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-282">È stato specificato il valore Variant per un qualificatore che non è un tipo di qualificatore valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_tipo di proprietà WBEM E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-284">2147749930 (0x8004102A)</span><span class="sxs-lookup"><span data-stu-id="e419e-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-285">Il tipo CIM specificato per una proprietà non è valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valore WBEM E non compreso nell' \_ \_ \_ \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="e419e-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-287">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="e419e-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-288">La richiesta è stata eseguita con un valore esterno all'intervallo o non è compatibile con il tipo.</span><span class="sxs-lookup"><span data-stu-id="e419e-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ non può \_ essere \_ singleton**</span><span class="sxs-lookup"><span data-stu-id="e419e-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-290">2147749932 (0x8004102C)</span><span class="sxs-lookup"><span data-stu-id="e419e-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-291">È stato effettuato un tentativo non valido di creare un singleton della classe, ad esempio quando la classe è derivata da una classe non singleton.</span><span class="sxs-lookup"><span data-stu-id="e419e-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ \_ tipo CIM non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-293">2147749933 (0x8004102D)</span><span class="sxs-lookup"><span data-stu-id="e419e-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-294">Il tipo CIM specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ metodo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-296">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="e419e-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-297">Il metodo richiesto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="e419e-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parametri del metodo WBEM E \_ non validi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-299">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="e419e-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-300">I parametri forniti per il metodo non sono validi.</span><span class="sxs-lookup"><span data-stu-id="e419e-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_proprietà di \_ sistema WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-302">2147749936 (0x80041030)</span><span class="sxs-lookup"><span data-stu-id="e419e-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-303">Si è verificato un tentativo di ottenere qualificatori su una proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="e419e-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_Proprietà WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-305">2147749937 (0x80041031)</span><span class="sxs-lookup"><span data-stu-id="e419e-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-306">Il tipo di proprietà non è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e419e-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**\_chiamata WBEM \_ E \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="e419e-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-308">2147749938 (0x80041032)</span><span class="sxs-lookup"><span data-stu-id="e419e-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-309">Il processo asincrono è stato annullato internamente o dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e419e-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="e419e-310">Si noti che a causa dell'intervallo e della natura dell'operazione asincrona, è possibile che l'operazione non sia stata effettivamente annullata.</span><span class="sxs-lookup"><span data-stu-id="e419e-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**chiusura di WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-312">2147749939 (0x80041033)</span><span class="sxs-lookup"><span data-stu-id="e419e-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-313">L'utente ha richiesto un'operazione mentre è in corso l'arresto di WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ Metodo propagato WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="e419e-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-315">2147749940 (0x80041034)</span><span class="sxs-lookup"><span data-stu-id="e419e-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-316">È stato effettuato un tentativo di riutilizzare un nome di metodo esistente da una classe padre e le firme non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="e419e-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_parametro WBEM E non \_ supportato \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-318">2147749941 (0x80041035)</span><span class="sxs-lookup"><span data-stu-id="e419e-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-319">Uno o più valori di parametro, come un testo della query, è troppo complesso o non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e419e-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="e419e-320">Per questo motivo, è necessario ripetere l'operazione con parametri più semplici.</span><span class="sxs-lookup"><span data-stu-id="e419e-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ E \_ \_ ID parametro \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="e419e-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-322">2147749942 (0x80041036)</span><span class="sxs-lookup"><span data-stu-id="e419e-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-323">Il parametro non è presente nella chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="e419e-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ID parametro WBEM E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-325">2147749943 (0x80041037)</span><span class="sxs-lookup"><span data-stu-id="e419e-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-326">Il parametro del metodo ha un qualificatore [**ID**](standard-wmi-qualifiers.md) non valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ID di parametro WBEM E non \_ consecutivi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-328">2147749944 (0x80041038)</span><span class="sxs-lookup"><span data-stu-id="e419e-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-329">Uno o più parametri del metodo hanno qualificatori [**ID**](standard-wmi-qualifiers.md) fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="e419e-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ ID parametro WBEM \_ E \_ in \_ retval**</span><span class="sxs-lookup"><span data-stu-id="e419e-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-331">2147749945 (0x80041039)</span><span class="sxs-lookup"><span data-stu-id="e419e-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-332">Il valore restituito per un metodo ha un qualificatore [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="e419e-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**\_percorso dell'oggetto WBEM E \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-334">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="e419e-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-335">Il percorso dell'oggetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**\_ \_ \_ \_ spazio disponibile su disco WBEM E esaurito \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-337">2147749947 (0x8004103B)</span><span class="sxs-lookup"><span data-stu-id="e419e-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-338">Lo spazio su disco è esaurito o è stato raggiunto il limite di 4 GB per il repository WMI (repository CIM).</span><span class="sxs-lookup"><span data-stu-id="e419e-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_buffer WBEM \_ E \_ troppo \_ piccolo**</span><span class="sxs-lookup"><span data-stu-id="e419e-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-340">2147749948 (0x8004103C)</span><span class="sxs-lookup"><span data-stu-id="e419e-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-341">Il buffer fornito è troppo piccolo per conservare tutti gli oggetti nell'enumeratore o per leggere una proprietà di stringa.</span><span class="sxs-lookup"><span data-stu-id="e419e-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM \_ E \_ \_ put Extension non supportata \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-343">2147749949 (0x8004103D)</span><span class="sxs-lookup"><span data-stu-id="e419e-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-344">Il provider non supporta l'operazione PUT richiesta.</span><span class="sxs-lookup"><span data-stu-id="e419e-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM \_ E \_ \_ tipo di oggetto sconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-346">2147749950 (0x8004103E)</span><span class="sxs-lookup"><span data-stu-id="e419e-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-347">Rilevato oggetto con tipo o versione non corretta durante il marshalling.</span><span class="sxs-lookup"><span data-stu-id="e419e-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_tipo di pacchetto WBEM E \_ sconosciuto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-349">2147749951 (0x8004103F)</span><span class="sxs-lookup"><span data-stu-id="e419e-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-350">È stato rilevato un pacchetto con un tipo o una versione non corretta durante il marshalling.</span><span class="sxs-lookup"><span data-stu-id="e419e-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**\_versione del marshalling E di WBEM non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="e419e-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-352">2147749952 (0x80041040)</span><span class="sxs-lookup"><span data-stu-id="e419e-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-353">La versione del pacchetto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e419e-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_firma del \_ marshalling E marshalling \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-355">2147749953 (0x80041041)</span><span class="sxs-lookup"><span data-stu-id="e419e-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-356">Il pacchetto sembra danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e419e-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_ \_ qualificatore WBEM E non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-358">2147749954 (0x80041042)</span><span class="sxs-lookup"><span data-stu-id="e419e-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-359">È stato effettuato un tentativo di mancata corrispondenza dei qualificatori, ad esempio inserendo \[ \] la chiave su un oggetto anziché una proprietà.</span><span class="sxs-lookup"><span data-stu-id="e419e-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ parametro non valido per WBEM E \_ duplicato \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-361">2147749955 (0x80041043)</span><span class="sxs-lookup"><span data-stu-id="e419e-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-362">Il parametro duplicato è stato dichiarato in un metodo CIM.</span><span class="sxs-lookup"><span data-stu-id="e419e-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ troppa \_ quantità di \_ dati**</span><span class="sxs-lookup"><span data-stu-id="e419e-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-364">2147749956 (0x80041044)</span><span class="sxs-lookup"><span data-stu-id="e419e-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-365">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="e419e-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ server \_ troppo \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="e419e-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-367">2147749957 (0x80041045)</span><span class="sxs-lookup"><span data-stu-id="e419e-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-368">La chiamata a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e419e-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="e419e-369">Il provider può rigenerare l'evento.</span><span class="sxs-lookup"><span data-stu-id="e419e-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**versione WBEM \_ E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-371">2147749958 (0x80041046)</span><span class="sxs-lookup"><span data-stu-id="e419e-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-372">La versione del qualificatore specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ riferimento circolare WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="e419e-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-374">2147749959 (0x80041047)</span><span class="sxs-lookup"><span data-stu-id="e419e-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-375">È stato effettuato un tentativo di creare un riferimento circolare (ad esempio, derivando una classe da se stessa).</span><span class="sxs-lookup"><span data-stu-id="e419e-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ aggiornamento della classe non supportato \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-377">2147749960 (0x80041048)</span><span class="sxs-lookup"><span data-stu-id="e419e-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-378">La classe specificata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e419e-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ non è possibile \_ modificare l' \_ ereditarietà della chiave \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-380">2147749961 (0x80041049)</span><span class="sxs-lookup"><span data-stu-id="e419e-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-381">È stato effettuato un tentativo di modificare una chiave quando le istanze o le sottoclassi usano già la chiave.</span><span class="sxs-lookup"><span data-stu-id="e419e-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ non può \_ modificare l' \_ ereditarietà degli indici \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-383">2147749968 (0x80041050)</span><span class="sxs-lookup"><span data-stu-id="e419e-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-384">È stato effettuato un tentativo di modificare un indice quando le istanze o le sottoclassi usano già l'indice.</span><span class="sxs-lookup"><span data-stu-id="e419e-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ troppe \_ \_ Proprietà**</span><span class="sxs-lookup"><span data-stu-id="e419e-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-386">2147749969 (0x80041051)</span><span class="sxs-lookup"><span data-stu-id="e419e-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-387">È stato effettuato un tentativo di creare un numero di proprietà maggiore di quello supportato dalla versione corrente della classe.</span><span class="sxs-lookup"><span data-stu-id="e419e-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**\_tipo di aggiornamento WBEM E non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="e419e-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-389">2147749970 (0x80041052)</span><span class="sxs-lookup"><span data-stu-id="e419e-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-390">La proprietà è stata ridefinita con un tipo in conflitto in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="e419e-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_sostituzione degli aggiornamenti WBEM E \_ \_ \_ non \_ consentita**</span><span class="sxs-lookup"><span data-stu-id="e419e-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-392">2147749971 (0x80041053)</span><span class="sxs-lookup"><span data-stu-id="e419e-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-393">Tentativo eseguito in una classe derivata per eseguire l'override di un qualificatore che non può essere sottoposto a override.</span><span class="sxs-lookup"><span data-stu-id="e419e-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ Metodo propagato WBEM E Update \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-395">2147749972 (0x80041054)</span><span class="sxs-lookup"><span data-stu-id="e419e-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-396">Il metodo è stato nuovamente dichiarato con una firma in conflitto in una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="e419e-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_Metodo WBEM \_ E \_ non \_ implementato**</span><span class="sxs-lookup"><span data-stu-id="e419e-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-398">2147749973 (0x80041055)</span><span class="sxs-lookup"><span data-stu-id="e419e-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-399">È stato effettuato un tentativo di eseguire un metodo non contrassegnato con \[ implementato \] in una classe rilevante.</span><span class="sxs-lookup"><span data-stu-id="e419e-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM \_ E \_ metodo \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="e419e-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="e419e-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e419e-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="e419e-402">È stato effettuato un tentativo di eseguire un metodo contrassegnato con \[ disabilitato \] .</span><span class="sxs-lookup"><span data-stu-id="e419e-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_aggiornamento WBEM E \_ \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="e419e-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-404">2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="e419e-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-405">Il servizio di aggiornamento è occupato con un'altra operazione.</span><span class="sxs-lookup"><span data-stu-id="e419e-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_query WBEM E non \_ analizzabile \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-407">2147749976 (0x80041058)</span><span class="sxs-lookup"><span data-stu-id="e419e-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-408">La sintassi della query di filtro non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ Not \_ - \_ classe di evento**</span><span class="sxs-lookup"><span data-stu-id="e419e-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-410">2147749977 (0x80041059)</span><span class="sxs-lookup"><span data-stu-id="e419e-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-411">La clausola from di una query di filtro fa riferimento a una classe che non è una classe di evento (non derivata da un [**\_ \_ evento**](--event.md)).</span><span class="sxs-lookup"><span data-stu-id="e419e-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ \_ gruppo mancante \_ entro**</span><span class="sxs-lookup"><span data-stu-id="e419e-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-413">2147749978 (0x8004105A)</span><span class="sxs-lookup"><span data-stu-id="e419e-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-414">È stata utilizzata una clausola GROUP BY senza la corrispondente clausola GROUP WITHIN.</span><span class="sxs-lookup"><span data-stu-id="e419e-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ \_ elenco di aggregazioni mancanti \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-416">2147749979 (0x8004105B)</span><span class="sxs-lookup"><span data-stu-id="e419e-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-417">È stata utilizzata una clausola GROUP BY.</span><span class="sxs-lookup"><span data-stu-id="e419e-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="e419e-418">L'aggregazione di tutte le proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e419e-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**\_Proprietà WBEM E \_ non è \_ \_ un \_ oggetto**</span><span class="sxs-lookup"><span data-stu-id="e419e-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-420">2147749980 (0x8004105C)</span><span class="sxs-lookup"><span data-stu-id="e419e-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-421">È stata utilizzata la notazione del punto in una proprietà che non è un oggetto incorporato.</span><span class="sxs-lookup"><span data-stu-id="e419e-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ aggregazione \_ per \_ oggetto**</span><span class="sxs-lookup"><span data-stu-id="e419e-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-423">2147749981 (0x8004105D)</span><span class="sxs-lookup"><span data-stu-id="e419e-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-424">Una clausola GROUP BY fa riferimento a una proprietà che è un oggetto incorporato senza l'utilizzo della notazione del punto.</span><span class="sxs-lookup"><span data-stu-id="e419e-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_query del provider WBEM E non \_ interpretabile \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-426">2147749983 (0x8004105F)</span><span class="sxs-lookup"><span data-stu-id="e419e-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-427">La query di registrazione del provider di eventi ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) non ha specificato le classi per cui sono stati forniti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="e419e-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ backup \_ Restore \_ WinMgmt \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="e419e-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-429">2147749984 (0x80041060)</span><span class="sxs-lookup"><span data-stu-id="e419e-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-430">È stata effettuata una richiesta per eseguire il backup o il ripristino del repository mentre era usato da WinMgmt.exe o dal processo SVCHOST che contiene il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**\_ \_ overflow coda WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="e419e-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-432">2147749985 (0x80041061)</span><span class="sxs-lookup"><span data-stu-id="e419e-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-433">Overflow della coda di recapito asincrono causato da un consumer di eventi troppo lento.</span><span class="sxs-lookup"><span data-stu-id="e419e-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**il \_ privilegio WBEM E non è stato \_ \_ \_ mantenuto**</span><span class="sxs-lookup"><span data-stu-id="e419e-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-435">2147749986 (0x80041062)</span><span class="sxs-lookup"><span data-stu-id="e419e-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-436">L'operazione non è riuscita perché il client non dispone dei privilegi di sicurezza necessari.</span><span class="sxs-lookup"><span data-stu-id="e419e-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_operatore WBEM E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-438">2147749987 (0x80041063)</span><span class="sxs-lookup"><span data-stu-id="e419e-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-439">Operatore non valido per questo tipo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="e419e-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ credenziali locali E \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="e419e-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-441">2147749988 (0x80041064)</span><span class="sxs-lookup"><span data-stu-id="e419e-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-442">L'utente ha specificato un nome utente/password/autorità in una connessione locale.</span><span class="sxs-lookup"><span data-stu-id="e419e-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="e419e-443">L'utente deve usare un nome utente/password vuoto e fare affidamento sulla sicurezza predefinita.</span><span class="sxs-lookup"><span data-stu-id="e419e-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ non può \_ essere \_ astratto**</span><span class="sxs-lookup"><span data-stu-id="e419e-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-445">2147749989 (0x80041065)</span><span class="sxs-lookup"><span data-stu-id="e419e-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-446">La classe è stata creata in modo astratto quando la relativa classe padre non è astratta.</span><span class="sxs-lookup"><span data-stu-id="e419e-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E \_ \_ oggetto modificato**</span><span class="sxs-lookup"><span data-stu-id="e419e-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-448">2147749990 (0x80041066)</span><span class="sxs-lookup"><span data-stu-id="e419e-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-449">L'oggetto modificato è stato scritto senza che il **flag WBEM usi il flag dei \_ \_ \_ \_ qualificatori modificati** specificato.</span><span class="sxs-lookup"><span data-stu-id="e419e-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_client WBEM \_ E \_ troppo \_ lento**</span><span class="sxs-lookup"><span data-stu-id="e419e-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-451">2147749991 (0x80041067)</span><span class="sxs-lookup"><span data-stu-id="e419e-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-452">Il client non ha recuperato gli oggetti in modo sufficientemente rapido da un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e419e-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="e419e-453">Questa costante viene restituita quando un client crea un oggetto di enumerazione, ma non recupera gli oggetti dall'enumeratore in modo tempestivo, causando il backup delle cache degli oggetti dell'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="e419e-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**\_descrittore di sicurezza WBEM E \_ null \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-455">2147749992 (0x80041068)</span><span class="sxs-lookup"><span data-stu-id="e419e-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-456">È stato utilizzato il descrittore di sicurezza null.</span><span class="sxs-lookup"><span data-stu-id="e419e-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**timeout di WBEM \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-458">2147749993 (0x80041069)</span><span class="sxs-lookup"><span data-stu-id="e419e-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-459">Timeout dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e419e-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**\_associazione WBEM E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="e419e-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="e419e-462">Associazione non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_operazione WBEM E \_ ambigua \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-464">2147749995 (0x8004106B)</span><span class="sxs-lookup"><span data-stu-id="e419e-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-465">L'operazione è ambigua.</span><span class="sxs-lookup"><span data-stu-id="e419e-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_violazione della \_ quota \_ E di WBEM**</span><span class="sxs-lookup"><span data-stu-id="e419e-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-467">2147749996 (0x8004106C)</span><span class="sxs-lookup"><span data-stu-id="e419e-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-468">WMI sta occupando troppa memoria.</span><span class="sxs-lookup"><span data-stu-id="e419e-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="e419e-469">Questo problema può essere causato dalla disponibilità di memoria insufficiente o da un utilizzo eccessivo della memoria da WMI.</span><span class="sxs-lookup"><span data-stu-id="e419e-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_conflitto di \_ transazioni WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-471">2147749997 (0x8004106D)</span><span class="sxs-lookup"><span data-stu-id="e419e-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-472">L'operazione ha causato un conflitto di transazioni.</span><span class="sxs-lookup"><span data-stu-id="e419e-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_rollback E \_ forzato di WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-474">2147749998 (0x8004106E)</span><span class="sxs-lookup"><span data-stu-id="e419e-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-475">Transazione forzata un rollback.</span><span class="sxs-lookup"><span data-stu-id="e419e-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM \_ E \_ \_ impostazioni locali non supportate**</span><span class="sxs-lookup"><span data-stu-id="e419e-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-477">2147749999 (0x8004106F)</span><span class="sxs-lookup"><span data-stu-id="e419e-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-478">Le impostazioni locali utilizzate nella chiamata non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="e419e-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E \_ handle \_ non \_ \_ aggiornati**</span><span class="sxs-lookup"><span data-stu-id="e419e-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-480">2147750000 (0x80041070)</span><span class="sxs-lookup"><span data-stu-id="e419e-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-481">Handle di oggetto non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e419e-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**\_connessione WBEM \_ E \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="e419e-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-483">2147750001 (0x80041071)</span><span class="sxs-lookup"><span data-stu-id="e419e-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-484">Connessione al database SQL non riuscita.</span><span class="sxs-lookup"><span data-stu-id="e419e-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_richiesta di \_ handle non valida per WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-486">2147750002 (0x80041072)</span><span class="sxs-lookup"><span data-stu-id="e419e-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-487">La richiesta dell'handle non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_nome della proprietà WBEM E \_ \_ \_ troppo \_ ampio**</span><span class="sxs-lookup"><span data-stu-id="e419e-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-489">2147750003 (0x80041073)</span><span class="sxs-lookup"><span data-stu-id="e419e-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-490">Il nome della proprietà contiene più di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e419e-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**il \_ nome della classe WBEM E è \_ \_ \_ troppo \_ ampio**</span><span class="sxs-lookup"><span data-stu-id="e419e-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-492">2147750004 (0x80041074)</span><span class="sxs-lookup"><span data-stu-id="e419e-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-493">Il nome della classe contiene più di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e419e-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**\_nome del metodo WBEM E \_ \_ \_ troppo \_ ampio**</span><span class="sxs-lookup"><span data-stu-id="e419e-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-495">2147750005 (0x80041075)</span><span class="sxs-lookup"><span data-stu-id="e419e-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-496">Il nome del metodo contiene più di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e419e-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_nome del \_ qualificatore WBEM E \_ \_ troppo \_ ampio**</span><span class="sxs-lookup"><span data-stu-id="e419e-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-498">2147750006 (0x80041076)</span><span class="sxs-lookup"><span data-stu-id="e419e-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-499">Il nome del qualificatore contiene più di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e419e-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_ \_ comando Riesegui WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-501">2147750007 (0x80041077)</span><span class="sxs-lookup"><span data-stu-id="e419e-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-502">È necessario eseguire di nuovo il comando SQL perché in SQL è presente un deadlock.</span><span class="sxs-lookup"><span data-stu-id="e419e-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="e419e-503">Questa operazione può essere restituita solo quando i dati vengono archiviati in un database SQL.</span><span class="sxs-lookup"><span data-stu-id="e419e-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**non \_ corrispondenza del database WBEM E \_ \_ ver \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-505">2147750008 (0x80041078)</span><span class="sxs-lookup"><span data-stu-id="e419e-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-506">La versione del database non corrisponde alla versione elaborata dal driver del repository.</span><span class="sxs-lookup"><span data-stu-id="e419e-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ veto \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="e419e-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-508">2147750009 (0x80041079)</span><span class="sxs-lookup"><span data-stu-id="e419e-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-509">WMI non è in grado di eseguire l'operazione di eliminazione perché il provider non lo consente.</span><span class="sxs-lookup"><span data-stu-id="e419e-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ veto \_ put**</span><span class="sxs-lookup"><span data-stu-id="e419e-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-511">2147750010 (0x8004107A)</span><span class="sxs-lookup"><span data-stu-id="e419e-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-512">WMI non è in grado di eseguire l'operazione Put perché il provider non lo consente.</span><span class="sxs-lookup"><span data-stu-id="e419e-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ impostazioni locali non valide per WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-514">2147750016 (0x80041080)</span><span class="sxs-lookup"><span data-stu-id="e419e-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-515">L'identificatore delle impostazioni locali specificato non è valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e419e-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_provider WBEM \_ E \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="e419e-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-517">2147750017 (0x80041081)</span><span class="sxs-lookup"><span data-stu-id="e419e-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-518">Il provider è sospeso.</span><span class="sxs-lookup"><span data-stu-id="e419e-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_sincronizzazione WBEM \_ E \_ necessaria**</span><span class="sxs-lookup"><span data-stu-id="e419e-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-520">2147750018 (0x80041082)</span><span class="sxs-lookup"><span data-stu-id="e419e-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-521">L'oggetto deve essere scritto nel repository WMI e recuperato di nuovo prima che l'operazione richiesta possa essere eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="e419e-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="e419e-522">Questa costante viene restituita quando è necessario eseguire il commit e il recupero di un oggetto per visualizzare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e419e-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ nessun \_ schema**</span><span class="sxs-lookup"><span data-stu-id="e419e-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-524">2147750019 (0x80041083)</span><span class="sxs-lookup"><span data-stu-id="e419e-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-525">Non è possibile completare l'operazione. non è disponibile alcuno schema.</span><span class="sxs-lookup"><span data-stu-id="e419e-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_provider WBEM \_ E \_ già \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="e419e-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-527">02147750020 (0x119FD010)</span><span class="sxs-lookup"><span data-stu-id="e419e-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-528">Impossibile registrare il provider perché è già registrato.</span><span class="sxs-lookup"><span data-stu-id="e419e-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_provider WBEM \_ E \_ non \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="e419e-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-530">2147750021 (0x80041085)</span><span class="sxs-lookup"><span data-stu-id="e419e-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-531">Il provider non è registrato.</span><span class="sxs-lookup"><span data-stu-id="e419e-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_errore di trasporto WBEM E \_ irreversibile \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-533">2147750022 (0x80041086)</span><span class="sxs-lookup"><span data-stu-id="e419e-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-534">Si è verificato un errore di trasporto irreversibile.</span><span class="sxs-lookup"><span data-stu-id="e419e-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_ \_ connessione crittografata WBEM E \_ \_ necessaria**</span><span class="sxs-lookup"><span data-stu-id="e419e-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-536">2147750023 (0x80041087)</span><span class="sxs-lookup"><span data-stu-id="e419e-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-537">L'utente ha tentato di impostare un nome computer o un dominio senza una connessione crittografata.</span><span class="sxs-lookup"><span data-stu-id="e419e-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**\_timeout del \_ provider WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-539">2147750024 (0x80041088)</span><span class="sxs-lookup"><span data-stu-id="e419e-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-540">Un provider non è riuscito a segnalare i risultati entro il timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="e419e-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ Nessuna \_ chiave**</span><span class="sxs-lookup"><span data-stu-id="e419e-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-542">2147750025 (0x80041089)</span><span class="sxs-lookup"><span data-stu-id="e419e-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-543">L'utente ha tentato di inserire un'istanza senza chiave definita.</span><span class="sxs-lookup"><span data-stu-id="e419e-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_provider WBEM \_ E \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="e419e-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-545">2147750026 (0x8004108A)</span><span class="sxs-lookup"><span data-stu-id="e419e-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-546">L'utente ha tentato di registrare un'istanza del provider ma il server COM per l'istanza del provider è stato scaricato.</span><span class="sxs-lookup"><span data-stu-id="e419e-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**registrazione di WBEMESS \_ E \_ \_ troppo \_ ampia**</span><span class="sxs-lookup"><span data-stu-id="e419e-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-548">2147753985 (0x80042001)</span><span class="sxs-lookup"><span data-stu-id="e419e-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-549">La registrazione del provider si sovrappone al dominio dell'evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="e419e-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**registrazione di WBEMESS \_ E \_ \_ troppo \_ precisa**</span><span class="sxs-lookup"><span data-stu-id="e419e-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-551">2147753986 (0x80042002)</span><span class="sxs-lookup"><span data-stu-id="e419e-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-552">Nella query non è stata utilizzata una clausola WITHIN.</span><span class="sxs-lookup"><span data-stu-id="e419e-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ AUTHZ \_ senza \_ privilegi**</span><span class="sxs-lookup"><span data-stu-id="e419e-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-554">2147753987 (0x80042003)</span><span class="sxs-lookup"><span data-stu-id="e419e-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-555">Il computer non dispone delle autorizzazioni necessarie per il dominio per supportare le funzioni di sicurezza correlate all'istanza di sottoscrizione creata.</span><span class="sxs-lookup"><span data-stu-id="e419e-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="e419e-556">Contattare l'amministratore di dominio per aggiungere il computer al gruppo di accesso di autorizzazione Windows.</span><span class="sxs-lookup"><span data-stu-id="e419e-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ Riprova \_ più tardi**</span><span class="sxs-lookup"><span data-stu-id="e419e-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-558">2147758081 (0x80043001)</span><span class="sxs-lookup"><span data-stu-id="e419e-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-559">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="e419e-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**\_ \_ contesa di risorse E di WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-561">2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="e419e-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-562">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="e419e-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ \_ Nome qualificatore previsto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-564">2147762177 (0x80044001)</span><span class="sxs-lookup"><span data-stu-id="e419e-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-565">Previsto un nome di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="e419e-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ previsto \_ semi**</span><span class="sxs-lookup"><span data-stu-id="e419e-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-567">2147762178 (0x80044002)</span><span class="sxs-lookup"><span data-stu-id="e419e-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-568">Previsto punto e virgola o ' ='.</span><span class="sxs-lookup"><span data-stu-id="e419e-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ \_ parentesi graffa di apertura prevista \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-570">2147762179 (0x80044003)</span><span class="sxs-lookup"><span data-stu-id="e419e-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-571">Prevista parentesi graffa di apertura.</span><span class="sxs-lookup"><span data-stu-id="e419e-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ \_ parentesi graffa di chiusura prevista \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-573">2147762180 (0x80044004)</span><span class="sxs-lookup"><span data-stu-id="e419e-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-574">Parentesi graffa di chiusura mancante o elemento di matrice non valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ parentesi chiusa \_ prevista**</span><span class="sxs-lookup"><span data-stu-id="e419e-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-576">2147762181 (0x80044005)</span><span class="sxs-lookup"><span data-stu-id="e419e-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-577">È prevista una parentesi di chiusura.</span><span class="sxs-lookup"><span data-stu-id="e419e-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ \_ parentesi chiuse \_ previste**</span><span class="sxs-lookup"><span data-stu-id="e419e-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-579">2147762182 (0x80044006)</span><span class="sxs-lookup"><span data-stu-id="e419e-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-580">Prevista parentesi di chiusura.</span><span class="sxs-lookup"><span data-stu-id="e419e-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valore costante non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-582">2147762183 (0x80044007)</span><span class="sxs-lookup"><span data-stu-id="e419e-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-583">Valore numerico non compreso nell'intervallo o nelle stringhe senza virgolette.</span><span class="sxs-lookup"><span data-stu-id="e419e-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ \_ identificatore di tipo previsto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-585">2147762184 (0x80044008)</span><span class="sxs-lookup"><span data-stu-id="e419e-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-586">È previsto un identificatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="e419e-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ \_ parentesi aperta \_ prevista**</span><span class="sxs-lookup"><span data-stu-id="e419e-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-588">2147762185 (0x80044009)</span><span class="sxs-lookup"><span data-stu-id="e419e-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-589">È prevista una parentesi aperta.</span><span class="sxs-lookup"><span data-stu-id="e419e-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ token non riconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-591">2147762186 (0x8004400A)</span><span class="sxs-lookup"><span data-stu-id="e419e-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-592">Token imprevisto nel file.</span><span class="sxs-lookup"><span data-stu-id="e419e-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ tipo non riconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-594">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="e419e-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-595">Identificatore di tipo non riconosciuto o non supportato.</span><span class="sxs-lookup"><span data-stu-id="e419e-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ \_ nome della proprietà prevista \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-597">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="e419e-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-598">Nome del metodo o della proprietà previsto.</span><span class="sxs-lookup"><span data-stu-id="e419e-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF \_ E \_ typedef \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="e419e-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-600">2147762189 (0x8004400D)</span><span class="sxs-lookup"><span data-stu-id="e419e-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-601">I typedef e i tipi enumerati non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e419e-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ alias imprevisto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-603">2147762190 (0x8004400E)</span><span class="sxs-lookup"><span data-stu-id="e419e-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-604">Solo un riferimento a un oggetto classe può avere un valore alias.</span><span class="sxs-lookup"><span data-stu-id="e419e-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ \_ inizializzazione di matrice imprevista \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-606">2147762191 (0x8004400F)</span><span class="sxs-lookup"><span data-stu-id="e419e-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-607">Inizializzazione di matrice imprevista.</span><span class="sxs-lookup"><span data-stu-id="e419e-607">Unexpected array initialization.</span></span> <span data-ttu-id="e419e-608">Le matrici devono essere dichiarate con \[ \] .</span><span class="sxs-lookup"><span data-stu-id="e419e-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi di modifica non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-610">2147762192 (0x80044010)</span><span class="sxs-lookup"><span data-stu-id="e419e-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-611">Sintassi del percorso dello spazio dei nomi non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ modifica duplicata non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-613">2147762193 (0x80044011)</span><span class="sxs-lookup"><span data-stu-id="e419e-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-614">Identificatori di modifica duplicati.</span><span class="sxs-lookup"><span data-stu-id="e419e-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**\_pragma WBEMMOF E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-616">2147762194 (0x80044012)</span><span class="sxs-lookup"><span data-stu-id="e419e-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-617">il [ \# pragma](pragma-namespace.md) deve essere seguito da una parola chiave valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi dello spazio dei nomi non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-619">2147762195 (0x80044013)</span><span class="sxs-lookup"><span data-stu-id="e419e-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-620">Sintassi del percorso dello spazio dei nomi non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ il \_ nome della classe previsto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-622">2147762196 (0x80044014)</span><span class="sxs-lookup"><span data-stu-id="e419e-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-623">Il carattere imprevisto nel nome della classe deve essere un identificatore.</span><span class="sxs-lookup"><span data-stu-id="e419e-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**tipo di WBEMMOF \_ E non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="e419e-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-625">2147762197 (0x80044015)</span><span class="sxs-lookup"><span data-stu-id="e419e-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-626">Il valore specificato non può essere creato nel tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="e419e-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ \_ nome alias \_ previsto**</span><span class="sxs-lookup"><span data-stu-id="e419e-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-628">2147762198 (0x80044016)</span><span class="sxs-lookup"><span data-stu-id="e419e-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-629">Il segno di dollaro deve essere seguito da un nome di alias come identificatore.</span><span class="sxs-lookup"><span data-stu-id="e419e-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ \_ dichiarazione di classe non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-631">2147762199 (0x80044017)</span><span class="sxs-lookup"><span data-stu-id="e419e-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-632">Dichiarazione di classe non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ \_ dichiarazione di istanza non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-634">2147762200 (0x80044018)</span><span class="sxs-lookup"><span data-stu-id="e419e-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-635">La dichiarazione dell'istanza non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-635">The instance declaration is not valid.</span></span> <span data-ttu-id="e419e-636">Deve iniziare con "instance of"</span><span class="sxs-lookup"><span data-stu-id="e419e-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ \_ dollaro previsto**</span><span class="sxs-lookup"><span data-stu-id="e419e-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-638">2147762201 (0x80044019)</span><span class="sxs-lookup"><span data-stu-id="e419e-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-639">È previsto un segno di dollaro.</span><span class="sxs-lookup"><span data-stu-id="e419e-639">Expected dollar sign.</span></span> <span data-ttu-id="e419e-640">Un alias nel formato "$name" deve seguire la parola chiave "As".</span><span class="sxs-lookup"><span data-stu-id="e419e-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_ \_ qualificatore WBEMMOF E CimType \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-642">2147762202 (0x8004401A)</span><span class="sxs-lookup"><span data-stu-id="e419e-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-643">Impossibile specificare il qualificatore "CIMTYPE" direttamente in un file MOF.</span><span class="sxs-lookup"><span data-stu-id="e419e-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="e419e-644">Usare la notazione di tipo standard.</span><span class="sxs-lookup"><span data-stu-id="e419e-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ Proprietà duplicata \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-646">2147762203 (0x8004401B)</span><span class="sxs-lookup"><span data-stu-id="e419e-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-647">Il nome di proprietà duplicato è stato trovato nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="e419e-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ \_ specifica dello spazio dei nomi non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-649">2147762204 (0x8004401C)</span><span class="sxs-lookup"><span data-stu-id="e419e-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-650">La sintassi dello spazio dei nomi non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="e419e-651">Non sono consentiti riferimenti ad altri server.</span><span class="sxs-lookup"><span data-stu-id="e419e-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ non \_ \_ compreso nell'intervallo**</span><span class="sxs-lookup"><span data-stu-id="e419e-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-653">2147762205 (0x8004401D)</span><span class="sxs-lookup"><span data-stu-id="e419e-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-654">Il valore non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="e419e-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**\_file WBEMMOF E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-656">2147762206 (0x8004401E)</span><span class="sxs-lookup"><span data-stu-id="e419e-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-657">Il file non è un file MOF di testo o un file MOF binario valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ E \_ alias \_ in \_ Embedded**</span><span class="sxs-lookup"><span data-stu-id="e419e-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-659">2147762207 (0x8004401F)</span><span class="sxs-lookup"><span data-stu-id="e419e-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-660">Gli oggetti incorporati non possono essere alias.</span><span class="sxs-lookup"><span data-stu-id="e419e-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**\_elem WBEMMOF E \_ null \_ array \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-662">2147762208 (0x80044020)</span><span class="sxs-lookup"><span data-stu-id="e419e-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-663">Gli elementi NULL in una matrice non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e419e-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF \_ E \_ \_ qualificatore duplicato**</span><span class="sxs-lookup"><span data-stu-id="e419e-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-665">2147762209 (0x80044021)</span><span class="sxs-lookup"><span data-stu-id="e419e-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-666">Il qualificatore è stato usato più di una volta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e419e-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ \_ tipo di sapore previsto \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-668">2147762210 (0x80044022)</span><span class="sxs-lookup"><span data-stu-id="e419e-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-669">È previsto un tipo di sapore, ad esempio **ToInstance**, **ToClass**, **EnableOverride** o **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="e419e-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_tipi di \_ sapore incompatibili con WBEMMOF E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-671">2147762211 (0x80044023)</span><span class="sxs-lookup"><span data-stu-id="e419e-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-672">La combinazione di **EnableOverride** e **DisableOverride** nello stesso qualificatore non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ più \_ alias**</span><span class="sxs-lookup"><span data-stu-id="e419e-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-674">2147762212 (0x80044024)</span><span class="sxs-lookup"><span data-stu-id="e419e-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-675">Non è possibile usare due volte un alias.</span><span class="sxs-lookup"><span data-stu-id="e419e-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ \_ TYPES2 Flavor incompatibili \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-677">2147762213 (0x80044025)</span><span class="sxs-lookup"><span data-stu-id="e419e-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-678">La **combinazione di** **Restricted** e **ToClass o ToClass** non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ non sono state \_ \_ restituite matrici**</span><span class="sxs-lookup"><span data-stu-id="e419e-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-680">2147762214 (0x80044026)</span><span class="sxs-lookup"><span data-stu-id="e419e-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-681">I metodi non possono restituire valori di matrice.</span><span class="sxs-lookup"><span data-stu-id="e419e-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ e \_ deve \_ essere \_ in \_ \_ uscita**</span><span class="sxs-lookup"><span data-stu-id="e419e-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-683">2147762215 (0x80044027)</span><span class="sxs-lookup"><span data-stu-id="e419e-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-684">Gli argomenti devono avere un qualificatore **in** o **out** .</span><span class="sxs-lookup"><span data-stu-id="e419e-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**\_sintassi WBEMMOF \_ E \_ flag non validi \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-686">2147762216 (0x80044028)</span><span class="sxs-lookup"><span data-stu-id="e419e-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-687">Sintassi di flag non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ e \_ \_ tipo di parentesi graffa prevista \_ o non \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-689">2147762217 (0x80044029)</span><span class="sxs-lookup"><span data-stu-id="e419e-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-690">Manca la parentesi graffa finale e il punto e virgola di una classe.</span><span class="sxs-lookup"><span data-stu-id="e419e-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E non \_ supportato \_ CIMV22 \_ qual \_ value**</span><span class="sxs-lookup"><span data-stu-id="e419e-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-692">2147762218 (0x8004402A)</span><span class="sxs-lookup"><span data-stu-id="e419e-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-693">Una funzionalità CIM versione 2,2 non è supportata per un valore qualificatore.</span><span class="sxs-lookup"><span data-stu-id="e419e-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ \_ tipo di dati CIMV22 \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e419e-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-695">2147762219 (0x8004402B)</span><span class="sxs-lookup"><span data-stu-id="e419e-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-696">Il tipo di dati CIM versione 2,2 non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e419e-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi DELETEINSTANCE non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-698">2147762220 (0x8004402C)</span><span class="sxs-lookup"><span data-stu-id="e419e-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-699">La sintassi dell'istanza Delete non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="e419e-700">Dovrebbe essere `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="e419e-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi di qualificatore non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-702">2147762221 (0x8004402D)</span><span class="sxs-lookup"><span data-stu-id="e419e-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-703">Sintassi del qualificatore non valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="e419e-704">Il valore dovrebbe essere `qualifiername:type=value,scope(class|instance), flavorname`.</span><span class="sxs-lookup"><span data-stu-id="e419e-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_ \_ qualificatore WBEMMOF E \_ usato \_ all'esterno dell' \_ ambito**</span><span class="sxs-lookup"><span data-stu-id="e419e-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-706">2147762222 (0x8004402E)</span><span class="sxs-lookup"><span data-stu-id="e419e-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-707">Il qualificatore viene usato al di fuori dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="e419e-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ errore durante la \_ creazione del \_ \_ file temporaneo**</span><span class="sxs-lookup"><span data-stu-id="e419e-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-709">2147762223 (0x8004402F)</span><span class="sxs-lookup"><span data-stu-id="e419e-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-710">Errore durante la creazione del file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="e419e-710">Error creating temporary file.</span></span> <span data-ttu-id="e419e-711">Il file temporaneo è una fase intermedia della compilazione MOF.</span><span class="sxs-lookup"><span data-stu-id="e419e-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**\_errore WBEMMOF \_ E \_ \_ file di inclusione non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-713">2147762224 (0x80044030)</span><span class="sxs-lookup"><span data-stu-id="e419e-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-714">Un file incluso nel file MOF tramite il comando per il preprocessore [ \# include](-include.md) non è valido.</span><span class="sxs-lookup"><span data-stu-id="e419e-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e419e-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ \_ sintassi DELETECLASS non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e419e-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e419e-716">2147762225 (0x80044031)</span><span class="sxs-lookup"><span data-stu-id="e419e-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="e419e-717">La sintassi per i comandi del preprocessore [ \# pragma DeleteInstance](pragma-deleteinstance.md) o [ \# pragma deleteclass](pragma-deleteclass.md) non è valida.</span><span class="sxs-lookup"><span data-stu-id="e419e-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e419e-718">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e419e-718">Requirements</span></span>



| <span data-ttu-id="e419e-719">Requisito</span><span class="sxs-lookup"><span data-stu-id="e419e-719">Requirement</span></span> | <span data-ttu-id="e419e-720">Valore</span><span class="sxs-lookup"><span data-stu-id="e419e-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e419e-721">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e419e-721">Minimum supported client</span></span><br/> | <span data-ttu-id="e419e-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e419e-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e419e-723">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e419e-723">Minimum supported server</span></span><br/> | <span data-ttu-id="e419e-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e419e-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e419e-725">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e419e-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="e419e-726"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="e419e-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="e419e-727">IDL</span><span class="sxs-lookup"><span data-stu-id="e419e-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e419e-728"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e419e-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e419e-729">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e419e-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e419e-730">Codici restituiti WMI</span><span class="sxs-lookup"><span data-stu-id="e419e-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

