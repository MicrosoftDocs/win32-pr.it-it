---
title: Metodi di proprietà IADsService (IADs. h)
description: Leggere e scrivere le proprietà descritte in questo argomento.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsService ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301478"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="ed6ae-104">Metodi di proprietà IADsService</span><span class="sxs-lookup"><span data-stu-id="ed6ae-104">IADsService Property Methods</span></span>

<span data-ttu-id="ed6ae-105">I metodi di proprietà dell'interfaccia [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) leggono e scrivono le proprietà descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="ed6ae-106">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ed6ae-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ed6ae-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed6ae-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ed6ae-108">**Dipendenze**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-108">**Dependencies**</span></span>
<span data-ttu-id="ed6ae-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-110">Matrice di nomi **BSTR** dei servizi o dei gruppi di carico che devono essere caricati per il caricamento del servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="ed6ae-111">La sintassi per la voce è "Service:" seguita dal nome del servizio o "Group:" seguito dal nome del gruppo di caricamento.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="ed6ae-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-114">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-114">**DisplayName**</span></span>
<span data-ttu-id="ed6ae-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-116">Nome descrittivo del servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="ed6ae-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-119">**ErrorControl**</span></span>
<span data-ttu-id="ed6ae-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-121">Azione da eseguire se il servizio non riesce all'avvio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="ed6ae-122">Di seguito sono riportati i valori validi per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="ed6ae-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\_errore del servizio ADS \_ \_ Ignora \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-124">Il programma di avvio registra l'errore, ma continua l'operazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="ed6ae-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>errore del servizio ADS- \_ \_ \_ normale \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-126">Il programma di avvio registra l'errore e visualizza una finestra di messaggio, ma continua l'operazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="ed6ae-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_errore grave del servizio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-128">Il programma di avvio registra l'errore.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-128">The startup program logs the error.</span></span> <span data-ttu-id="ed6ae-129">Se viene avviata la configurazione Last-know-valido, l'operazione di avvio continua.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="ed6ae-130">In caso contrario, il sistema viene riavviato con l'ultima configurazione ben nota.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="ed6ae-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_errore critico del servizio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-132">Il programma di avvio registra l'errore, se possibile.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="ed6ae-133">Se è in corso l'avvio della configurazione Last-know-valido, l'operazione di avvio non riesce.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="ed6ae-134">In caso contrario, il sistema viene riavviato con l'ultima configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="ed6ae-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-136">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-137">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-137">**HostComputer**</span></span>
<span data-ttu-id="ed6ae-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-139">Stringa ADsPath dell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="ed6ae-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-141">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="ed6ae-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-144">Nome del gruppo di ordini di carico di cui questo servizio è membro.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="ed6ae-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-146">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-147">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-147">**Path**</span></span>
<span data-ttu-id="ed6ae-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-149">Percorso e nome file dell'eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="ed6ae-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-151">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-152">**ServiceAccountName**</span></span>
<span data-ttu-id="ed6ae-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-154">Nome dell'account utilizzato dal servizio per l'autenticazione all'avvio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="ed6ae-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-156">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-157">**ServiceAccountPath**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="ed6ae-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-159">Percorso dell'account specificato dalla proprietà **ServiceAccountPath** .</span><span class="sxs-lookup"><span data-stu-id="ed6ae-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="ed6ae-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-161">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-162">**ServiceType**</span></span>
<span data-ttu-id="ed6ae-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-164">Descrizione del modo in cui un servizio presenta se stesso nel computer host.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="ed6ae-165">Questa proprietà può essere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="ed6ae-166">DRIVER del kernel del servizio ADS \* \* \* \* \_ \_ \_ (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ed6ae-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="ed6ae-167">\_Driver del \_ file System del servizio ADS \* \* \* \* \_ \_ (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ed6ae-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="ed6ae-168">\_Processo del servizio ADS \* \* \* \* \_ \_ (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="ed6ae-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="ed6ae-169">Processo di condivisione del servizio ADS \* \* \* \* \_ \_ \_ (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="ed6ae-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="ed6ae-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-171">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-172">**Tipo di avvio**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-172">**StartType**</span></span>
<span data-ttu-id="ed6ae-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-174">Determina come avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-174">Determines how to start the service.</span></span> <span data-ttu-id="ed6ae-175">Di seguito sono riportati i valori validi per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="ed6ae-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>avvio \_ avvio del servizio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-177">Il servizio è un driver di dispositivo avviato dal caricatore di sistema.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="ed6ae-178">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="ed6ae-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_avvio del sistema del servizio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-180">Il servizio è un driver di dispositivo avviato dalla funzione **IoInitSystem** .</span><span class="sxs-lookup"><span data-stu-id="ed6ae-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="ed6ae-181">Questo valore è valido solo per i servizi del driver.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="ed6ae-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_avvio automatico del servizio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-183">Il servizio verrà avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="ed6ae-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_ \_ avvio richiesta servizio ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-185">Il servizio verrà avviato da Gestione controllo servizi quando un processo chiama la funzione [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="ed6ae-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="ed6ae-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_servizio ADS \_ disabilitato \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ed6ae-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ed6ae-187">Impossibile avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-187">The service cannot be started.</span></span> <span data-ttu-id="ed6ae-188">Tenta di avviare il risultato del servizio nel servizio errori codice di errore **\_ \_ disabilitato**.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="ed6ae-189">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-190">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-191">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-191">**StartupParameters**</span></span>
<span data-ttu-id="ed6ae-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-193">Parametri passati al servizio all'avvio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="ed6ae-194">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-195">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ed6ae-196">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-196">**Version**</span></span>
<span data-ttu-id="ed6ae-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ed6ae-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="ed6ae-198">Versione del servizio.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="ed6ae-199">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ed6ae-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ed6ae-200">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ed6ae-201">Esempio</span><span class="sxs-lookup"><span data-stu-id="ed6ae-201">Examples</span></span>

<span data-ttu-id="ed6ae-202">Nell'esempio di codice seguente viene illustrato come elencare tutti i servizi di sistema disponibili in esecuzione nel computer host, "computer", insieme al percorso per trovare i file eseguibili dei servizi.</span><span class="sxs-lookup"><span data-stu-id="ed6ae-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="ed6ae-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed6ae-203">Requirements</span></span>



| <span data-ttu-id="ed6ae-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed6ae-204">Requirement</span></span> | <span data-ttu-id="ed6ae-205">Valore</span><span class="sxs-lookup"><span data-stu-id="ed6ae-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed6ae-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed6ae-206">Minimum supported client</span></span><br/> | <span data-ttu-id="ed6ae-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed6ae-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed6ae-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed6ae-208">Minimum supported server</span></span><br/> | <span data-ttu-id="ed6ae-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed6ae-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed6ae-210">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed6ae-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed6ae-211"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed6ae-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ed6ae-212">DLL</span><span class="sxs-lookup"><span data-stu-id="ed6ae-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed6ae-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed6ae-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ed6ae-214">IID</span><span class="sxs-lookup"><span data-stu-id="ed6ae-214">IID</span></span><br/>                      | <span data-ttu-id="ed6ae-215">IID \_ IADsService è definito come 68AF66E0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="ed6ae-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ed6ae-216">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed6ae-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed6ae-217">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="ed6ae-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="ed6ae-218">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="ed6ae-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

