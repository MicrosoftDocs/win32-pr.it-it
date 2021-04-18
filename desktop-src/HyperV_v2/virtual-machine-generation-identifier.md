---
description: Windows 8 e Windows Server 2012 presentano la possibilità per il software in esecuzione in una macchina virtuale di rilevare che è possibile che si sia verificato un evento di spostamento temporale.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificatore di generazione macchina virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317177"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="09a51-103">Identificatore di generazione macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="09a51-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="09a51-104">Windows 8 e Windows Server 2012 presentano la possibilità per il software in esecuzione in una macchina virtuale di rilevare che è possibile che si sia verificato un evento di spostamento temporale.</span><span class="sxs-lookup"><span data-stu-id="09a51-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="09a51-105">Gli eventi di spostamento temporale possono verificarsi a causa di un'applicazione di uno snapshot della macchina virtuale o del ripristino di un backup di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09a51-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="09a51-106">Per ulteriori informazioni su questa funzionalità, vedere l' [ID di generazione della macchina virtuale white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span><span class="sxs-lookup"><span data-stu-id="09a51-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="09a51-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="09a51-107">Prerequisites</span></span>

<span data-ttu-id="09a51-108">Per usare l'identificatore di generazione della macchina virtuale all'interno di una macchina virtuale, la macchina virtuale deve essere conforme a quanto segue.</span><span class="sxs-lookup"><span data-stu-id="09a51-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="09a51-109">La macchina virtuale deve essere in esecuzione in un hypervisor che implementa il supporto per gli identificatori di generazione delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="09a51-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="09a51-110">Attualmente, questi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="09a51-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="09a51-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09a51-111">Windows 8</span></span>
    -   <span data-ttu-id="09a51-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09a51-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="09a51-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="09a51-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="09a51-114">Nella macchina virtuale deve essere in esecuzione un sistema operativo guest con supporto per l'identificatore di generazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09a51-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="09a51-115">Attualmente, questi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="09a51-115">Currently, these are the following.</span></span>

    <span data-ttu-id="09a51-116">I sistemi operativi seguenti hanno il supporto nativo per l'identificatore di generazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09a51-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="09a51-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09a51-117">Windows 8</span></span>
    -   <span data-ttu-id="09a51-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09a51-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="09a51-119">Il funzionamento seguente può essere utilizzato come sistema operativo guest se i servizi di integrazione Hyper-V da Windows 8 o Windows Server 2012 sono installati.</span><span class="sxs-lookup"><span data-stu-id="09a51-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="09a51-120">Windows Server 2008 R2 con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="09a51-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="09a51-121">Windows 7 con Service Pack 1 (SP1):</span><span class="sxs-lookup"><span data-stu-id="09a51-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="09a51-122">Windows Server 2008 con Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="09a51-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="09a51-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09a51-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="09a51-124">Windows Server 2003 con Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="09a51-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="09a51-125">Windows Vista con Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="09a51-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="09a51-126">Windows XP con Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="09a51-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="09a51-127">Acquisizione dell'identificatore di generazione della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="09a51-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="09a51-128">Per ottenere a livello di codice l'identificatore di generazione della macchina virtuale, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="09a51-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="09a51-129">Per il corretto funzionamento, è necessario eseguire le operazioni seguenti con privilegi di amministratore o di sistema.</span><span class="sxs-lookup"><span data-stu-id="09a51-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="09a51-130">Includere il file di intestazione "vmgenerationcounter. h" nell'app.</span><span class="sxs-lookup"><span data-stu-id="09a51-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="09a51-131">Il file di intestazione contiene le definizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="09a51-131">The header file contains these definitions:</span></span>
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  <span data-ttu-id="09a51-132">Aprire un handle per il " \\ \\ . \\ VmGenerationCounter "dispositivo che utilizza la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="09a51-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="09a51-133">In alternativa, è possibile usare la gestione PnP per utilizzare il GUID dell'interfaccia del dispositivo **\_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4E60-8e1c-0ccf4927e319}).</span><span class="sxs-lookup"><span data-stu-id="09a51-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="09a51-134">Questi oggetti non saranno presenti se l'app non è in esecuzione in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09a51-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="09a51-135">Inviare il comando IOCTL [**\_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL al driver per recuperare l'identificatore di generazione.</span><span class="sxs-lookup"><span data-stu-id="09a51-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="09a51-136">IOCTL [**\_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL opera in una delle due modalità, *polling* e basato su *eventi*.</span><span class="sxs-lookup"><span data-stu-id="09a51-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="09a51-137">Per eseguire IOCTL in modalità di polling, è necessario inviare il IOCTL con un buffer di input di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="09a51-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="09a51-138">In risposta a questo, il driver recupera l'identificatore di generazione corrente, lo scrive nel buffer di output e completa l'IOCTL.</span><span class="sxs-lookup"><span data-stu-id="09a51-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="09a51-139">Per eseguire IOCTL in modalità basata su eventi, inviare il comando IOCTL con un buffer di input che contiene un identificatore di generazione esistente.</span><span class="sxs-lookup"><span data-stu-id="09a51-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="09a51-140">In risposta a questo, il driver attende fino a quando l'identificatore di generazione corrente diventa diverso dall'identificatore di generazione passato.</span><span class="sxs-lookup"><span data-stu-id="09a51-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="09a51-141">Quando l'identificatore di generazione viene modificato, il driver scrive l'identificatore di generazione corrente nel buffer di output e completa l'IOCTL.</span><span class="sxs-lookup"><span data-stu-id="09a51-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="09a51-142">In entrambe le modalità, il formato e la lunghezza del buffer di output sono determinati dalla struttura della [**macchina virtuale \_ GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .</span><span class="sxs-lookup"><span data-stu-id="09a51-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="09a51-143">La modalità di polling è supportata in tutti i sistemi operativi guest elencati sopra.</span><span class="sxs-lookup"><span data-stu-id="09a51-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="09a51-144">La modalità basata su eventi è supportata solo in Windows Vista con SP2, Windows Server 2008 con SP2 e sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="09a51-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="09a51-145">Nei sistemi operativi precedenti, l'IOCTL avrà esito negativo e l'errore del codice di errore **\_ non è \_ supportato** quando viene eseguito in modalità basata su eventi.</span><span class="sxs-lookup"><span data-stu-id="09a51-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="09a51-146">È possibile che l'identificatore di generazione cambi tra il momento in cui viene recuperato dal driver e il momento in cui il comando IOCTL viene completato.</span><span class="sxs-lookup"><span data-stu-id="09a51-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="09a51-147">Ciò può comportare la ricezione di dati non aggiornati nell'app client.</span><span class="sxs-lookup"><span data-stu-id="09a51-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="09a51-148">Per evitare questo problema, l'app client può usare la modalità guidata dagli eventi per assicurarsi che vengano apprese informazioni sugli aggiornamenti all'identificatore di generazione.</span><span class="sxs-lookup"><span data-stu-id="09a51-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="09a51-149">Accettando l'identificatore corrente dell'app client come input, la modalità basata su eventi evita potenziali race condition che potrebbero causare la mancata notifica da parte del chiamante.</span><span class="sxs-lookup"><span data-stu-id="09a51-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="09a51-150">Nell'esempio di codice seguente viene illustrato come eseguire le azioni precedenti per ottenere l'identificatore di generazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09a51-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="09a51-151">Il codice seguente deve essere eseguito con privilegi di amministratore o di sistema per funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="09a51-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="09a51-152">Determinare se si è verificato un evento di spostamento temporale</span><span class="sxs-lookup"><span data-stu-id="09a51-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="09a51-153">Dopo aver ottenuto l'identificatore di generazione della macchina virtuale, è necessario archiviarlo per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="09a51-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="09a51-154">Prima che l'app esegua un'operazione sensibile al tempo, ad esempio il commit in un database, è necessario ottenere nuovamente l'identificatore di generazione e confrontarlo con il valore archiviato.</span><span class="sxs-lookup"><span data-stu-id="09a51-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="09a51-155">Se l'identificatore è stato modificato, significa che si è verificato un evento di spostamento temporale e che l'app deve agire in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="09a51-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
