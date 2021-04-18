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
# <a name="virtual-machine-generation-identifier"></a>Identificatore di generazione macchina virtuale

Windows 8 e Windows Server 2012 presentano la possibilità per il software in esecuzione in una macchina virtuale di rilevare che è possibile che si sia verificato un evento di spostamento temporale. Gli eventi di spostamento temporale possono verificarsi a causa di un'applicazione di uno snapshot della macchina virtuale o del ripristino di un backup di una macchina virtuale. Per ulteriori informazioni su questa funzionalità, vedere l' [ID di generazione della macchina virtuale white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).

## <a name="prerequisites"></a>Prerequisiti

Per usare l'identificatore di generazione della macchina virtuale all'interno di una macchina virtuale, la macchina virtuale deve essere conforme a quanto segue.

-   La macchina virtuale deve essere in esecuzione in un hypervisor che implementa il supporto per gli identificatori di generazione delle macchine virtuali. Attualmente, questi sono i seguenti:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   Nella macchina virtuale deve essere in esecuzione un sistema operativo guest con supporto per l'identificatore di generazione della macchina virtuale. Attualmente, questi sono i seguenti.

    I sistemi operativi seguenti hanno il supporto nativo per l'identificatore di generazione della macchina virtuale.

    -   Windows 8
    -   Windows Server 2012
    -   

    Il funzionamento seguente può essere utilizzato come sistema operativo guest se i servizi di integrazione Hyper-V da Windows 8 o Windows Server 2012 sono installati.

    -   Windows Server 2008 R2 con Service Pack 1 (SP1)
    -   Windows 7 con Service Pack 1 (SP1):
    -   Windows Server 2008 con Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 con Service Pack 2 (SP2)
    -   Windows Vista con Service Pack 2 (SP2)
    -   Windows XP con Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Acquisizione dell'identificatore di generazione della macchina virtuale

Per ottenere a livello di codice l'identificatore di generazione della macchina virtuale, seguire questa procedura.

> [!Note]  
> Per il corretto funzionamento, è necessario eseguire le operazioni seguenti con privilegi di amministratore o di sistema.

 

1.  Includere il file di intestazione "vmgenerationcounter. h" nell'app. Il file di intestazione contiene le definizioni seguenti:
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

    

2.  Aprire un handle per il " \\ \\ . \\ VmGenerationCounter "dispositivo che utilizza la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . In alternativa, è possibile usare la gestione PnP per utilizzare il GUID dell'interfaccia del dispositivo **\_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4E60-8e1c-0ccf4927e319}). Questi oggetti non saranno presenti se l'app non è in esecuzione in una macchina virtuale.
3.  Inviare il comando IOCTL [**\_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL al driver per recuperare l'identificatore di generazione.

    IOCTL [**\_ VMGENCOUNTER \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL opera in una delle due modalità, *polling* e basato su *eventi*.

    Per eseguire IOCTL in modalità di polling, è necessario inviare il IOCTL con un buffer di input di lunghezza zero. In risposta a questo, il driver recupera l'identificatore di generazione corrente, lo scrive nel buffer di output e completa l'IOCTL.

    Per eseguire IOCTL in modalità basata su eventi, inviare il comando IOCTL con un buffer di input che contiene un identificatore di generazione esistente. In risposta a questo, il driver attende fino a quando l'identificatore di generazione corrente diventa diverso dall'identificatore di generazione passato. Quando l'identificatore di generazione viene modificato, il driver scrive l'identificatore di generazione corrente nel buffer di output e completa l'IOCTL.

    In entrambe le modalità, il formato e la lunghezza del buffer di output sono determinati dalla struttura della [**macchina virtuale \_ GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .

    La modalità di polling è supportata in tutti i sistemi operativi guest elencati sopra. La modalità basata su eventi è supportata solo in Windows Vista con SP2, Windows Server 2008 con SP2 e sistemi operativi successivi. Nei sistemi operativi precedenti, l'IOCTL avrà esito negativo e l'errore del codice di errore **\_ non è \_ supportato** quando viene eseguito in modalità basata su eventi.

    È possibile che l'identificatore di generazione cambi tra il momento in cui viene recuperato dal driver e il momento in cui il comando IOCTL viene completato. Ciò può comportare la ricezione di dati non aggiornati nell'app client. Per evitare questo problema, l'app client può usare la modalità guidata dagli eventi per assicurarsi che vengano apprese informazioni sugli aggiornamenti all'identificatore di generazione. Accettando l'identificatore corrente dell'app client come input, la modalità basata su eventi evita potenziali race condition che potrebbero causare la mancata notifica da parte del chiamante.

Nell'esempio di codice seguente viene illustrato come eseguire le azioni precedenti per ottenere l'identificatore di generazione della macchina virtuale.

> [!Note]  
> Il codice seguente deve essere eseguito con privilegi di amministratore o di sistema per funzionare correttamente.

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Determinare se si è verificato un evento di spostamento temporale

Dopo aver ottenuto l'identificatore di generazione della macchina virtuale, è necessario archiviarlo per un uso futuro. Prima che l'app esegua un'operazione sensibile al tempo, ad esempio il commit in un database, è necessario ottenere nuovamente l'identificatore di generazione e confrontarlo con il valore archiviato. Se l'identificatore è stato modificato, significa che si è verificato un evento di spostamento temporale e che l'app deve agire in modo appropriato.

 

 
