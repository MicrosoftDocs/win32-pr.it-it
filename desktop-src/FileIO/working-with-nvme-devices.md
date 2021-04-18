---
description: Informazioni su come usare dispositivi NVMe ad alta velocità dall'applicazione Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Utilizzo delle unità NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309524"
---
# <a name="working-with-nvme-drives"></a><span data-ttu-id="09db7-103">Utilizzo delle unità NVMe</span><span class="sxs-lookup"><span data-stu-id="09db7-103">Working with NVMe drives</span></span>

<span data-ttu-id="09db7-104">**Si applica a:**</span><span class="sxs-lookup"><span data-stu-id="09db7-104">**Applies to:**</span></span>

-   <span data-ttu-id="09db7-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="09db7-105">Windows 10</span></span>
-   <span data-ttu-id="09db7-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="09db7-106">Windows Server 2016</span></span>

<span data-ttu-id="09db7-107">Informazioni su come usare dispositivi NVMe ad alta velocità dall'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="09db7-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="09db7-108">L'accesso al dispositivo viene abilitato tramite **StorNVMe.sys**, il driver interno introdotto per la prima volta in Windows Server 2012 R2 e Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="09db7-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="09db7-109">È anche disponibile per i dispositivi Windows 7 tramite una correzione a caldo KB.</span><span class="sxs-lookup"><span data-stu-id="09db7-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="09db7-110">In Windows 10 sono state introdotte diverse nuove funzionalità, incluso un meccanismo pass-through per i comandi NVMe specifici del fornitore e gli aggiornamenti a IOCTL esistenti.</span><span class="sxs-lookup"><span data-stu-id="09db7-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="09db7-111">Questo argomento fornisce una panoramica delle API di uso generale che è possibile usare per accedere alle unità NVMe in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="09db7-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="09db7-112">Vengono inoltre descritte le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="09db7-112">It also describes:</span></span>

-   <span data-ttu-id="09db7-113">Come inviare un comando NVMe specifico del fornitore con [pass-through](#pass-through-mechanism)</span><span class="sxs-lookup"><span data-stu-id="09db7-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="09db7-114">Come [inviare un comando identifica, Ottieni funzionalità o Ottieni pagine di log](#protocol-specific-queries) all'unità NVMe</span><span class="sxs-lookup"><span data-stu-id="09db7-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="09db7-115">Come [ottenere informazioni sulla temperatura](#temperature-queries) da un'unità NVMe</span><span class="sxs-lookup"><span data-stu-id="09db7-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="09db7-116">Come eseguire i comandi di modifica del comportamento, ad esempio l' [impostazione delle soglie di temperatura](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="09db7-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="09db7-117">API per l'uso di unità NVMe</span><span class="sxs-lookup"><span data-stu-id="09db7-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="09db7-118">È possibile usare le API generali seguenti per accedere alle unità NVMe in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="09db7-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="09db7-119">Queste API si trovano in **winioctl. h** per le applicazioni in modalità utente e **ntddstor. h** per i driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="09db7-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="09db7-120">Per ulteriori informazioni sui file di intestazione, vedere [file di intestazione](#header-files).</span><span class="sxs-lookup"><span data-stu-id="09db7-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="09db7-121">[**IOCTL \_ \_ \_ Comando del protocollo di archiviazione**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : usare questo IOCTL con la struttura dei comandi del **\_ protocollo \_ di archiviazione** per emettere i comandi NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="09db7-122">Questo IOCTL Abilita NVMe pass-through e supporta il log degli effetti del comando in NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="09db7-123">È possibile usarlo con comandi specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="09db7-124">Per altre informazioni, vedere [meccanismo pass-through](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="09db7-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="09db7-125">[**Archiviazione \_ \_Comando protocollo**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : questa struttura del buffer di input include un campo **ReturnStatus** che può essere usato per segnalare i valori di stato seguenti.</span><span class="sxs-lookup"><span data-stu-id="09db7-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="09db7-126">**stato del protocollo di archiviazione \_ \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="09db7-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="09db7-127">**stato del protocollo di archiviazione \_ \_ \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="09db7-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="09db7-128">**\_errore di \_ stato del protocollo di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="09db7-129">**\_ \_ \_ richiesta non valida per lo stato del protocollo di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="09db7-130">**stato del protocollo di archiviazione \_ \_ \_ senza \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="09db7-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="09db7-131">**stato del protocollo di archiviazione \_ \_ \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="09db7-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="09db7-132">**\_ \_ \_ sovraccarico dei dati sullo stato del protocollo di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="09db7-133">**\_risorse stato protocollo di archiviazione \_ \_ insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="09db7-134">**\_lo stato del protocollo di archiviazione \_ non è \_ \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="09db7-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="09db7-135">[**IOCTL \_ \_ \_ Proprietà query di archiviazione**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : usare questo IOCTL con la struttura della **\_ \_ query della proprietà di archiviazione** per recuperare le informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09db7-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="09db7-136">Per altre informazioni, vedere [query specifiche del protocollo](#protocol-specific-queries) e [query di temperatura](#temperature-queries).</span><span class="sxs-lookup"><span data-stu-id="09db7-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="09db7-137">[**Archiviazione \_ PROPERTY \_ query**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : questa struttura include i campi **PropertyId** e **AdditionalParameters** per specificare i dati su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="09db7-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="09db7-138">Nel file **PropertyId** , usare l'enumerazione **\_ \_ ID proprietà di archiviazione** per specificare il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="09db7-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="09db7-139">Usare il campo **AdditionalParameters** per specificare ulteriori dettagli, a seconda del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="09db7-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="09db7-140">Per i dati specifici del protocollo, usare la struttura **\_ \_ \_ dei dati specifica del protocollo di archiviazione** nel campo **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="09db7-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="09db7-141">Per i dati relativi alla temperatura, usare la struttura **\_ \_ info temperature di archiviazione** nel campo **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="09db7-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="09db7-142">[**Archiviazione \_ \_ID proprietà**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : questa enumerazione include nuovi valori che consentono **alla \_ \_ \_ proprietà di query di archiviazione IOCTL** di recuperare informazioni sulla temperatura e sul protocollo.</span><span class="sxs-lookup"><span data-stu-id="09db7-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="09db7-143">**StorageAdapterProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="09db7-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="09db7-144">**StorageDeviceProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="09db7-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="09db7-145">Usare uno di questi ID proprietà specifici del protocollo in combinazione con **\_ \_ \_ i dati specifici del protocollo di archiviazione** per recuperare i dati specifici del protocollo nella struttura del [**\_ \_ \_ descrittore dei dati del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="09db7-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="09db7-146">**StorageAdapterTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="09db7-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="09db7-147">**StorageDeviceTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="09db7-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="09db7-148">Usare uno di questi ID di proprietà della temperatura per recuperare i dati sulla temperatura nella struttura del [**\_ \_ \_ descrittore dei dati della temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="09db7-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="09db7-149">[**Archiviazione \_ \_ \_ Dati specifici del protocollo**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : recuperare i dati specifici del NVMe quando questa struttura viene usata per il campo **AdditionalParameters** della **\_ \_ query della proprietà di archiviazione** e viene specificato un valore di enumerazione del [**\_ \_ \_ \_ tipo di dati NVMe del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) .</span><span class="sxs-lookup"><span data-stu-id="09db7-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="09db7-150">Usare uno dei valori del **\_ tipo di \_ \_ dati NVME \_ del protocollo di archiviazione** seguenti nel campo **DataType** della struttura di **\_ \_ \_ dati specifica del protocollo di archiviazione** :</span><span class="sxs-lookup"><span data-stu-id="09db7-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="09db7-151">Usare **NVMeDataTypeIdentify** per ottenere identifica dati del controller o identificare i dati dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="09db7-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="09db7-152">Usare **NVMeDataTypeLogPage** per ottenere le pagine di log (inclusi i dati intelligenti/di integrità).</span><span class="sxs-lookup"><span data-stu-id="09db7-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="09db7-153">Usare **NVMeDataTypeFeature** per ottenere le funzionalità dell'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="09db7-154">[**Archiviazione \_ \_Informazioni sulla temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : questa struttura viene utilizzata per conservare dati di temperatura specifici.</span><span class="sxs-lookup"><span data-stu-id="09db7-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="09db7-155">Viene usato nel **\_ \_ \_ descrittore di dati TEMERATURE di archiviazione** per restituire i risultati di una query di temperatura.</span><span class="sxs-lookup"><span data-stu-id="09db7-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="09db7-156">[**IOCTL \_ \_Soglia di \_ temperatura \_ del set di archiviazione**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : usare questo IOCTL con la struttura della **\_ \_ soglia di temperatura di archiviazione** per impostare le soglie di temperatura.</span><span class="sxs-lookup"><span data-stu-id="09db7-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="09db7-157">Per altre informazioni, vedere [comandi di modifica del comportamento](#behavior-changing-commands).</span><span class="sxs-lookup"><span data-stu-id="09db7-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="09db7-158">[**Archiviazione \_ \_Soglia temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : questa struttura viene utilizzata come buffer di input per specificare la soglia di temperatura.</span><span class="sxs-lookup"><span data-stu-id="09db7-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="09db7-159">Il campo di **sovrasoglia** (booleano) specifica se il campo della **soglia** è il valore della soglia superiore o meno. in caso contrario, è il valore di soglia sotto.</span><span class="sxs-lookup"><span data-stu-id="09db7-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="09db7-160">Meccanismo pass-through</span><span class="sxs-lookup"><span data-stu-id="09db7-160">Pass-through mechanism</span></span>

<span data-ttu-id="09db7-161">I comandi che non sono definiti nella specifica NVMe sono i più difficili da gestire per il sistema operativo host. l'host non è in grado di comprendere gli effetti che i comandi possono avere sul dispositivo di destinazione, l'infrastruttura esposta (dimensioni di spazi dei nomi/blocchi) e il relativo comportamento.</span><span class="sxs-lookup"><span data-stu-id="09db7-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="09db7-162">Per portare a termine tali comandi specifici del dispositivo tramite lo stack di archiviazione di Windows, un nuovo meccanismo pass-through consente di inviare tramite pipe i comandi specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="09db7-163">Questa pipe pass-through facilita anche lo sviluppo di strumenti di gestione e test.</span><span class="sxs-lookup"><span data-stu-id="09db7-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="09db7-164">Tuttavia, questo meccanismo pass-through richiede l'uso del log degli effetti del comando.</span><span class="sxs-lookup"><span data-stu-id="09db7-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="09db7-165">Inoltre, StoreNVMe.sys richiede che tutti i comandi, non solo i comandi pass-through, siano descritti nel log degli effetti dei comandi.</span><span class="sxs-lookup"><span data-stu-id="09db7-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09db7-166">StorNVMe.sys e Storport.sys bloccherà qualsiasi comando in un dispositivo, se non è descritto nel log degli effetti dei comandi.</span><span class="sxs-lookup"><span data-stu-id="09db7-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="09db7-167">Supporto del log degli effetti del comando</span><span class="sxs-lookup"><span data-stu-id="09db7-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="09db7-168">Il log degli effetti del comando (come descritto in comandi supportati ed effetti, sezione 5.10.1.5 della [specifica NVMe 1,2](https://nvmexpress.org/specifications)) consente di descrivere gli effetti dei comandi specifici del fornitore insieme ai comandi definiti dalla specifica.</span><span class="sxs-lookup"><span data-stu-id="09db7-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="09db7-169">Ciò facilita la convalida del supporto del comando e l'ottimizzazione del comportamento del comando e pertanto deve essere implementato per l'intero set di comandi supportati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09db7-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="09db7-170">Le condizioni seguenti descrivono il risultato della modalità di invio del comando in base alla voce del log degli effetti dei comandi.</span><span class="sxs-lookup"><span data-stu-id="09db7-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="09db7-171">Per qualsiasi comando specifico descritto nel log degli effetti del comando...</span><span class="sxs-lookup"><span data-stu-id="09db7-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="09db7-172">**Durante** le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="09db7-172">**While**:</span></span>

-   <span data-ttu-id="09db7-173">Il comando supportato (CSUPP) è impostato su' 1', a indicare che il comando è supportato dal controller (bit 01)</span><span class="sxs-lookup"><span data-stu-id="09db7-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="09db7-174">Quando CSUPP è impostato su' 0' (a indicare che il comando non è supportato) il comando verrà bloccato</span><span class="sxs-lookup"><span data-stu-id="09db7-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="09db7-175">**E se** viene impostata una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="09db7-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="09db7-176">La modifica della funzionalità del controller (CCC) è impostata su' 1' a indicare che il comando può modificare le funzionalità del controller (bit 04)</span><span class="sxs-lookup"><span data-stu-id="09db7-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="09db7-177">La modifica dell'inventario dello spazio dei nomi (NIC) è impostata su' 1', a indicare che il comando può modificare il numero o le funzionalità per più spazi dei nomi (bit 03)</span><span class="sxs-lookup"><span data-stu-id="09db7-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="09db7-178">La modifica della funzionalità dello spazio dei nomi (NCC) è impostata su' 1', a indicare che il comando può modificare le funzionalità di un singolo spazio dei nomi (bit 02)</span><span class="sxs-lookup"><span data-stu-id="09db7-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="09db7-179">L'invio e l'esecuzione del comando (CSE) è impostato su 001B o 010B, a indicare che il comando può essere inviato quando non vi sono altri comandi in attesa dello stesso o di uno spazio dei nomi e che un altro comando non deve essere inviato allo stesso o a uno spazio dei nomi fino al completamento del comando (BITS 18:16)</span><span class="sxs-lookup"><span data-stu-id="09db7-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="09db7-180">Il comando verrà **quindi** inviato come unico comando in attesa per l'adapter.</span><span class="sxs-lookup"><span data-stu-id="09db7-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="09db7-181">**Else if**:</span><span class="sxs-lookup"><span data-stu-id="09db7-181">**Else if**:</span></span>

-   <span data-ttu-id="09db7-182">L'invio e l'esecuzione del comando (CSE) è impostato su 001B, a indicare che il comando può essere inviato quando non vi sono altri comandi in attesa per lo stesso spazio dei nomi e che un altro comando non deve essere inviato allo stesso spazio dei nomi fino al completamento del comando (BITS 18:16)</span><span class="sxs-lookup"><span data-stu-id="09db7-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="09db7-183">Il comando verrà **quindi** inviato come unico comando in attesa all'oggetto numero di unità logica (lun).</span><span class="sxs-lookup"><span data-stu-id="09db7-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="09db7-184">**In caso contrario**, il comando viene inviato con altri comandi in attesa senza inibizione.</span><span class="sxs-lookup"><span data-stu-id="09db7-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="09db7-185">Ad esempio, se un comando specifico del fornitore viene inviato al dispositivo per recuperare informazioni statistiche che non sono definite da specifiche, non è necessario alcun rischio per modificare il comportamento o la funzionalità del dispositivo per eseguire I comandi di I/O.</span><span class="sxs-lookup"><span data-stu-id="09db7-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="09db7-186">Tali richieste possono essere gestite in parallelo all'I/O e non è necessario sospendere la ripresa.</span><span class="sxs-lookup"><span data-stu-id="09db7-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="09db7-187">Uso del \_ comando IOCTL storage \_ Protocol \_ per inviare comandi</span><span class="sxs-lookup"><span data-stu-id="09db7-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="09db7-188">Il pass-through può essere eseguito tramite [**il \_ \_ \_ comando IOCTL Storage Protocol**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introdotto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="09db7-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="09db7-189">Questo IOCTL è stato progettato per avere un comportamento simile a quello delle IOCTL di pass-through SCSI e ATA esistenti, per inviare un comando incorporato al dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09db7-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="09db7-190">Tramite questo IOCTL è possibile inviare il pass-through a un dispositivo di archiviazione, inclusa un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="09db7-191">Ad esempio, in NVMe, IOCTL consentirà l'invio dei seguenti codici di comando.</span><span class="sxs-lookup"><span data-stu-id="09db7-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="09db7-192">Comandi amministrativi specifici del fornitore (C0h – FFh)</span><span class="sxs-lookup"><span data-stu-id="09db7-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="09db7-193">Comandi NVMe specifici del fornitore (80H – FFh)</span><span class="sxs-lookup"><span data-stu-id="09db7-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="09db7-194">Come per tutti gli altri IOCTL, usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare il comando IOCTL pass-through.</span><span class="sxs-lookup"><span data-stu-id="09db7-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="09db7-195">IOCTL viene popolato usando la struttura del buffer di input del [**\_ \_ comando del protocollo di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) disponibile in **ntddstor. h**.</span><span class="sxs-lookup"><span data-stu-id="09db7-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="09db7-196">Popolare il campo di **comando** con il comando specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-196">Populate the **Command** field with the vendor-specific command.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



<span data-ttu-id="09db7-197">Il comando specifico del fornitore da inviare deve essere popolato nel campo evidenziato sopra.</span><span class="sxs-lookup"><span data-stu-id="09db7-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="09db7-198">Si noti che il log degli effetti del comando deve essere implementato per i comandi pass-through.</span><span class="sxs-lookup"><span data-stu-id="09db7-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="09db7-199">In particolare, questi comandi devono essere segnalati come supportati nel log degli effetti del comando. per ulteriori informazioni, vedere la sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="09db7-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="09db7-200">Si noti inoltre che i campi PRP sono specifici del driver, pertanto le applicazioni che inviano comandi possono lasciarle come 0.</span><span class="sxs-lookup"><span data-stu-id="09db7-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="09db7-201">Infine, questo IOCTL pass-through viene utilizzato per l'invio di comandi specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="09db7-202">Per inviare altri comandi NVMe amministrativi o non specifici del fornitore, ad esempio l'identificazione, questo IOCTL pass-through non deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="09db7-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="09db7-203">Ad esempio, è necessario usare la **\_ \_ \_ proprietà query di archiviazione IOCTL** per identificare o ottenere le pagine del log.</span><span class="sxs-lookup"><span data-stu-id="09db7-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="09db7-204">Per altre informazioni, vedere la sezione successiva, [query specifiche del protocollo](/windows).</span><span class="sxs-lookup"><span data-stu-id="09db7-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="09db7-205">Non aggiornare il firmware tramite il meccanismo pass-through</span><span class="sxs-lookup"><span data-stu-id="09db7-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="09db7-206">I comandi per il download e l'attivazione del firmware non devono essere inviati tramite il pass-through.</span><span class="sxs-lookup"><span data-stu-id="09db7-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="09db7-207">**IOCTL \_ Il \_ \_ comando del protocollo di archiviazione** deve essere usato solo per i comandi specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="09db7-208">Usare invece le IOCTL di archiviazione generali seguenti (introdotte in Windows 10) per evitare che le applicazioni usino direttamente la \_ versione SCSI miniport del firmware IOCTL.</span><span class="sxs-lookup"><span data-stu-id="09db7-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="09db7-209">I driver di archiviazione convertiranno il IOCTL in un comando SCSI o nella \_ versione miniport SCSI di IOCTL per il miniport.</span><span class="sxs-lookup"><span data-stu-id="09db7-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="09db7-210">Queste IOCTL sono consigliate per lo sviluppo di strumenti di aggiornamento del firmware in Windows 10 e Windows Server 2016:</span><span class="sxs-lookup"><span data-stu-id="09db7-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="09db7-211">**\_informazioni sul \_ firmware di archiviazione \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="09db7-212">**\_download del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="09db7-213">**\_attivazione del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="09db7-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="09db7-214">Per ottenere informazioni sull'archiviazione e aggiornare il firmware, Windows supporta anche i cmdlet di PowerShell per eseguire questa operazione rapidamente:</span><span class="sxs-lookup"><span data-stu-id="09db7-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="09db7-215">Per aggiornare il firmware in NVMe in Windows 8.1, usare \_ il \_ firmware miniport SCSI IOCTL \_ .</span><span class="sxs-lookup"><span data-stu-id="09db7-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="09db7-216">Questo IOCTL non è stato sottoportato a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="09db7-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="09db7-217">Per ulteriori informazioni, vedere [aggiornamento del firmware per un dispositivo NVMe in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span><span class="sxs-lookup"><span data-stu-id="09db7-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="09db7-218">Restituzione di errori tramite il meccanismo pass-through</span><span class="sxs-lookup"><span data-stu-id="09db7-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="09db7-219">Analogamente alle IOCTL pass-through SCSI e ATA, quando un comando/richiesta viene inviato al miniport o al dispositivo, l'IOCTL restituisce se l'operazione ha avuto esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="09db7-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="09db7-220">Nella struttura [**dei \_ \_ comandi del protocollo di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , IOCTL restituisce lo stato tramite il campo **ReturnStatus** .</span><span class="sxs-lookup"><span data-stu-id="09db7-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="09db7-221">Esempio: invio di un comando specifico del fornitore</span><span class="sxs-lookup"><span data-stu-id="09db7-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="09db7-222">In questo esempio, un comando arbitrario specifico del fornitore viene inviato tramite pass-through a un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="09db7-223">Il codice seguente alloca un buffer, Inizializza una query e quindi invia il comando al dispositivo tramite DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="09db7-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



<span data-ttu-id="09db7-224">In questo esempio, si prevede `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` se il comando è riuscito al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09db7-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="09db7-225">Query specifiche del protocollo</span><span class="sxs-lookup"><span data-stu-id="09db7-225">Protocol-specific queries</span></span>

<span data-ttu-id="09db7-226">Windows 8.1 introdotta la [**\_ proprietà di \_ query \_ di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="09db7-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="09db7-227">In Windows 10, il IOCTL è stato migliorato per supportare le funzionalità di NVMe richieste comunemente, ad esempio **ottenere le pagine del log**, ottenere le **funzionalità** e **identificare**.</span><span class="sxs-lookup"><span data-stu-id="09db7-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="09db7-228">In questo modo è possibile recuperare informazioni specifiche di NVMe a scopo di monitoraggio e inventario.</span><span class="sxs-lookup"><span data-stu-id="09db7-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="09db7-229">Di seguito è riportato il buffer di input per IOCTL, la [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (da Windows 10).</span><span class="sxs-lookup"><span data-stu-id="09db7-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="09db7-230">Quando si usa la [**\_ \_ \_ proprietà query di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per recuperare le informazioni specifiche del protocollo NVMe nel [**\_ \_ \_ descrittore di dati del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configurare la struttura della [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) come segue:</span><span class="sxs-lookup"><span data-stu-id="09db7-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="09db7-231">Allocare un buffer che può contenere sia [**una \_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) che una struttura di [**\_ \_ \_ dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .</span><span class="sxs-lookup"><span data-stu-id="09db7-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="09db7-232">Impostare il campo **PropertyId** su **StorageAdapterProtocolSpecificProperty** o **StorageDeviceProtocolSpecificProperty** rispettivamente per una richiesta controller o dispositivo/spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="09db7-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="09db7-233">Impostare il campo **QueryType** su **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="09db7-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="09db7-234">Riempire la [**struttura \_ \_ \_ dei dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) con i valori desiderati.</span><span class="sxs-lookup"><span data-stu-id="09db7-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="09db7-235">L'inizio dei **\_ \_ \_ dati specifici del protocollo di archiviazione** è il campo **AdditionalParameters** della [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span><span class="sxs-lookup"><span data-stu-id="09db7-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="09db7-236">Di seguito è illustrata la struttura [**\_ \_ \_ dei dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (da Windows 10).</span><span class="sxs-lookup"><span data-stu-id="09db7-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



<span data-ttu-id="09db7-237">Per specificare un tipo di informazioni specifiche del protocollo NVMe, configurare la struttura dei [**\_ \_ \_ dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) come segue:</span><span class="sxs-lookup"><span data-stu-id="09db7-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="09db7-238">Impostare il campo **ProtocolType** su **ProtocolTypeNVMe**.</span><span class="sxs-lookup"><span data-stu-id="09db7-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="09db7-239">Impostare il campo **DataType** su un valore di enumerazione definito [**dal \_ \_ tipo di \_ dati \_ NVME del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span><span class="sxs-lookup"><span data-stu-id="09db7-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="09db7-240">Usare **NVMeDataTypeIdentify** per ottenere identifica dati del controller o identificare i dati dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="09db7-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="09db7-241">Usare **NVMeDataTypeLogPage** per ottenere le pagine di log (inclusi i dati intelligenti/di integrità).</span><span class="sxs-lookup"><span data-stu-id="09db7-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="09db7-242">Usare **NVMeDataTypeFeature** per ottenere le funzionalità dell'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="09db7-243">Quando **ProtocolTypeNVMe** viene usato come **ProtocolType**, è possibile recuperare le query per le informazioni specifiche del protocollo in parallelo con altre i/O sull'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="09db7-244">Negli esempi seguenti vengono illustrate le query specifiche del protocollo NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="09db7-245">Esempio: NVMe identificare la query</span><span class="sxs-lookup"><span data-stu-id="09db7-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="09db7-246">In questo esempio la richiesta di **Identificazione** viene inviata a un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="09db7-247">Il codice seguente inizializza la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="09db7-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



<span data-ttu-id="09db7-248">Si noti che il chiamante deve allocare un singolo buffer contenente \_ \_ la query della proprietà di archiviazione e le dimensioni dei \_ dati specifici del protocollo di archiviazione \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="09db7-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="09db7-249">In questo esempio viene usato lo stesso buffer per l'input e l'output della query della proprietà.</span><span class="sxs-lookup"><span data-stu-id="09db7-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="09db7-250">Questo è il motivo per cui il buffer allocato ha una dimensione di "offset del campo \_ ( \_ query della proprietà \_ di archiviazione, AdditionalParameters) + sizeof ( \_ dati specifici del protocollo di archiviazione \_ \_ ) + \_ dimensioni massime del \_ log NVME \_ ".</span><span class="sxs-lookup"><span data-stu-id="09db7-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="09db7-251">Sebbene sia possibile allocare buffer distinti sia per l'input che per l'output, è consigliabile usare un singolo buffer per eseguire query sulle informazioni correlate a NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="09db7-252">Esempio: NVMe get log Pages query</span><span class="sxs-lookup"><span data-stu-id="09db7-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="09db7-253">In questo esempio, in base a quello precedente, la richiesta _ *get log Pages*\* viene inviata a un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="09db7-254">Il codice seguente prepara la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="09db7-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="09db7-255">Esempio: NVMe Get features query</span><span class="sxs-lookup"><span data-stu-id="09db7-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="09db7-256">In questo esempio, in base a quello precedente, la richiesta _ *Get features*\* viene inviata a un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="09db7-257">Il codice seguente prepara la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="09db7-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a><span data-ttu-id="09db7-258">Set specifico del protocollo</span><span class="sxs-lookup"><span data-stu-id="09db7-258">Protocol-specific set</span></span>

<span data-ttu-id="09db7-259">Da Windows 10 19H1, il IOCTL_STORAGE_SET_PROPERTY è stato migliorato per supportare le funzionalità di NVMe set.</span><span class="sxs-lookup"><span data-stu-id="09db7-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="09db7-260">Il buffer di input per il IOCTL_STORAGE_SET_PROPERTY è illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="09db7-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

<span data-ttu-id="09db7-261">Quando si usa IOCTL_STORAGE_SET_PROPERTY per impostare la funzionalità NVMe, configurare la struttura di STORAGE_PROPERTY_SET come segue:</span><span class="sxs-lookup"><span data-stu-id="09db7-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="09db7-262">Allocare un buffer che può contenere sia un STORAGE_PROPERTY_SET che una struttura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT;</span><span class="sxs-lookup"><span data-stu-id="09db7-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="09db7-263">Impostare il campo PropertyID su StorageAdapterProtocolSpecificProperty o StorageDeviceProtocolSpecificProperty rispettivamente per una richiesta controller o dispositivo/spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="09db7-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="09db7-264">Riempire la struttura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT con i valori desiderati.</span><span class="sxs-lookup"><span data-stu-id="09db7-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="09db7-265">L'inizio del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT è il campo AdditionalParameters di STORAGE_PROPERTY_SET.</span><span class="sxs-lookup"><span data-stu-id="09db7-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="09db7-266">Di seguito è illustrata la struttura del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT.</span><span class="sxs-lookup"><span data-stu-id="09db7-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

<span data-ttu-id="09db7-267">Per specificare un tipo di funzionalità NVMe da impostare, configurare la struttura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="09db7-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="09db7-268">Impostare il campo ProtocolType su ProtocolTypeNvme;</span><span class="sxs-lookup"><span data-stu-id="09db7-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="09db7-269">Impostare il campo DataType sul valore di enumerazione NVMeDataTypeFeature definito da STORAGE_PROTOCOL_NVME_DATA_TYPE;</span><span class="sxs-lookup"><span data-stu-id="09db7-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="09db7-270">Gli esempi seguenti illustrano il set di funzionalità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="09db7-271">Esempio: NVMe set features</span><span class="sxs-lookup"><span data-stu-id="09db7-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="09db7-272">In questo esempio la richiesta set features viene inviata a un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="09db7-273">Il codice seguente prepara la struttura dei dati del set e quindi invia il comando al dispositivo tramite DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="09db7-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a><span data-ttu-id="09db7-274">Query di temperatura</span><span class="sxs-lookup"><span data-stu-id="09db7-274">Temperature queries</span></span>

<span data-ttu-id="09db7-275">In Windows 10, [**la \_ \_ \_ proprietà query di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) può essere usata anche per eseguire query sui dati di temperatura dai dispositivi NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="09db7-276">Per recuperare le informazioni sulla temperatura da un'unità NVMe [**nel \_ \_ \_ descrittore di dati della temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configurare la struttura della [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) come segue:</span><span class="sxs-lookup"><span data-stu-id="09db7-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="09db7-277">Allocare un buffer che può contenere una struttura di [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .</span><span class="sxs-lookup"><span data-stu-id="09db7-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="09db7-278">Impostare il campo **PropertyId** su **StorageAdapterTemperatureProperty** o **StorageDeviceTemperatureProperty** rispettivamente per una richiesta controller o dispositivo/spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="09db7-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="09db7-279">Impostare il campo **QueryType** su **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="09db7-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="09db7-280">Di seguito è riportata la struttura delle [**\_ \_ informazioni sulla temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (da Windows 10).</span><span class="sxs-lookup"><span data-stu-id="09db7-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a><span data-ttu-id="09db7-281">Comandi di modifica del comportamento</span><span class="sxs-lookup"><span data-stu-id="09db7-281">Behavior changing commands</span></span>

<span data-ttu-id="09db7-282">I comandi che modificano gli attributi dei dispositivi o potenzialmente influire sul comportamento del dispositivo sono più difficili da gestire con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="09db7-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="09db7-283">Se gli attributi del dispositivo cambiano in fase di esecuzione durante l'elaborazione dell'I/O, possono verificarsi problemi di sincronizzazione o integrità dei dati se non vengono gestiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="09db7-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="09db7-284">Il comando **set-features** di NVMe è un valido esempio di un comando di modifica del comportamento.</span><span class="sxs-lookup"><span data-stu-id="09db7-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="09db7-285">Consente la modifica del meccanismo di arbitraggio e l'impostazione delle soglie di temperatura.</span><span class="sxs-lookup"><span data-stu-id="09db7-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="09db7-286">Per assicurarsi che i dati in corso non siano a rischio quando i comandi set che influiscono sul comportamento vengono inviati, verranno sospese tutte le operazioni di I/O nel dispositivo NVMe, le code di svuotamento e i buffer di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="09db7-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="09db7-287">Una volta eseguito correttamente il comando set, l'I/O viene ripreso (se possibile).</span><span class="sxs-lookup"><span data-stu-id="09db7-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="09db7-288">Se non è possibile riprendere l'I/O, potrebbe essere necessaria la reimpostazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09db7-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="09db7-289">Impostazione delle soglie di temperatura</span><span class="sxs-lookup"><span data-stu-id="09db7-289">Setting temperature thresholds</span></span>

<span data-ttu-id="09db7-290">Windows 10 ha introdotto la [**soglia di temperatura del \_ set di archiviazione \_ \_ \_ IOCTL**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), un IOCTL per ottenere e impostare le soglie di temperatura.</span><span class="sxs-lookup"><span data-stu-id="09db7-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="09db7-291">È anche possibile usarlo per ottenere la temperatura corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09db7-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="09db7-292">Il buffer di input/output per questo IOCTL è la struttura delle [**\_ \_ informazioni sulla temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , dalla sezione di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="09db7-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="09db7-293">Esempio: impostazione della temperatura eccessiva della soglia</span><span class="sxs-lookup"><span data-stu-id="09db7-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="09db7-294">In questo esempio viene impostata la temperatura eccessiva di soglia di un'unità NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="09db7-295">Il codice seguente prepara il comando e quindi lo invia al dispositivo tramite DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="09db7-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="09db7-296">Impostazione delle funzionalità specifiche del fornitore</span><span class="sxs-lookup"><span data-stu-id="09db7-296">Setting vendor-specific features</span></span>

<span data-ttu-id="09db7-297">Senza il log degli effetti del comando, il driver non conosce le ramificazioni del comando.</span><span class="sxs-lookup"><span data-stu-id="09db7-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="09db7-298">Questo è il motivo per cui il log degli effetti del comando è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="09db7-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="09db7-299">Consente al sistema operativo di determinare se un comando ha un effetto elevato e se può essere inviato in parallelo con altri comandi all'unità.</span><span class="sxs-lookup"><span data-stu-id="09db7-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="09db7-300">Il log degli effetti del comando non è ancora sufficientemente granulare per includere i comandi **Set-Feature** specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="09db7-301">Per questo motivo, non è ancora possibile inviare comandi **Set-Feature** specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="09db7-302">Tuttavia, è possibile usare il meccanismo pass-through, descritto in precedenza, per inviare comandi specifici del fornitore.</span><span class="sxs-lookup"><span data-stu-id="09db7-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="09db7-303">Per altre informazioni, vedere [meccanismo pass-through](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="09db7-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="09db7-304">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="09db7-304">Header files</span></span>

<span data-ttu-id="09db7-305">I file seguenti sono rilevanti per lo sviluppo di NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="09db7-306">Questi file sono inclusi in [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="09db7-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="09db7-307">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="09db7-307">Header file</span></span>    | <span data-ttu-id="09db7-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09db7-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09db7-309">**ntddstor. h**</span><span class="sxs-lookup"><span data-stu-id="09db7-309">**ntddstor.h**</span></span> | <span data-ttu-id="09db7-310">Definisce costanti e tipi per l'accesso ai driver della classe di archiviazione dalla modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="09db7-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="09db7-311">**nVMe. h**</span><span class="sxs-lookup"><span data-stu-id="09db7-311">**nvme.h**</span></span>     | <span data-ttu-id="09db7-312">Per altre strutture di dati correlate a NVMe.</span><span class="sxs-lookup"><span data-stu-id="09db7-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="09db7-313">**winioctl. h**</span><span class="sxs-lookup"><span data-stu-id="09db7-313">**winioctl.h**</span></span> | <span data-ttu-id="09db7-314">Per le definizioni globali del comando IOCTL Win32, incluse le API di archiviazione per le applicazioni in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="09db7-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
