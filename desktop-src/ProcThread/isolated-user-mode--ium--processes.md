---
description: In Windows 10 è stata introdotta una nuova funzionalità di sicurezza denominata Virtual Secure Mode (VSM).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Processi IUM (isolated User Mode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564204"
---
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="55d86-103">Processi IUM (isolated User Mode)</span><span class="sxs-lookup"><span data-stu-id="55d86-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="55d86-104">In Windows 10 è stata introdotta una nuova funzionalità di sicurezza denominata Virtual Secure Mode (VSM).</span><span class="sxs-lookup"><span data-stu-id="55d86-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="55d86-105">VSM sfrutta l'hypervisor Hyper-V e la modalità stecca (Second Level Address Translation) per creare un set di modalità denominate Virtual Trust Levels (VTLs).</span><span class="sxs-lookup"><span data-stu-id="55d86-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="55d86-106">Questa nuova architettura software crea un limite di sicurezza per impedire che i processi in esecuzione in un VTL accedano alla memoria di un altro VTL.</span><span class="sxs-lookup"><span data-stu-id="55d86-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="55d86-107">Il vantaggio di questo isolamento include la mitigazione aggiuntiva dagli exploit del kernel, proteggendo al tempo stesso gli asset, ad esempio gli hash delle password e le chiavi Kerberos.</span><span class="sxs-lookup"><span data-stu-id="55d86-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="55d86-108">Il diagramma 1 illustra il modello tradizionale di modalità kernel e il codice in modalità utente in esecuzione rispettivamente nell'anello 0 e nell'anello 3 della CPU.</span><span class="sxs-lookup"><span data-stu-id="55d86-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="55d86-109">In questo nuovo modello, il codice in esecuzione nel modello tradizionale viene eseguito in VTL0 e non può accedere al VTL1 con privilegi più elevati, in cui il kernel protetto e la modalità utente isolata (IUM) eseguono codice.</span><span class="sxs-lookup"><span data-stu-id="55d86-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="55d86-110">VTLs sono gerarchie significative che il codice in esecuzione in VTL1 è più privilegiato del codice in esecuzione in VTL0.</span><span class="sxs-lookup"><span data-stu-id="55d86-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="55d86-111">L'isolamento VTL viene creato dall'hypervisor di Hyper-V che assegna memoria in fase di avvio usando la conversione degli indirizzi di secondo livello.</span><span class="sxs-lookup"><span data-stu-id="55d86-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="55d86-112">Continua in modo dinamico durante l'esecuzione del sistema, proteggendo la memoria, il kernel protetto specifica la necessità di protezione da VTL0 perché verrà usato per contenere segreti.</span><span class="sxs-lookup"><span data-stu-id="55d86-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="55d86-113">Quando vengono allocati blocchi di memoria separati per due VTLs, viene creato un ambiente di runtime sicuro per VTL1 assegnando blocchi di memoria esclusivi a VTL1 e VTL0 con le autorizzazioni di accesso appropriate.</span><span class="sxs-lookup"><span data-stu-id="55d86-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="55d86-114">**Diagramma 1-architettura IUM**</span><span class="sxs-lookup"><span data-stu-id="55d86-114">**Diagram 1 - IUM Architecture**</span></span>

![diagramma 1-architettura IUM](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="55d86-116">Trustlets</span><span class="sxs-lookup"><span data-stu-id="55d86-116">Trustlets</span></span>

<span data-ttu-id="55d86-117">Trustlets (noti anche come processi attendibili, processi protetti o processi IUM) sono programmi in esecuzione come processi IUM in VSM.</span><span class="sxs-lookup"><span data-stu-id="55d86-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="55d86-118">Completano le chiamate di sistema eseguendone il marshalling nel kernel di Windows in esecuzione in VTL0 ring 0.</span><span class="sxs-lookup"><span data-stu-id="55d86-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="55d86-119">VSM crea un ambiente di esecuzione ridotto che include il kernel sicuro piccolo in esecuzione in VTL1 (isolato dal kernel e dai driver in esecuzione in VTL0).</span><span class="sxs-lookup"><span data-stu-id="55d86-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="55d86-120">Il vantaggio di sicurezza è l'isolamento delle pagine della modalità utente trustlet in VTL1 dai driver in esecuzione nel kernel VTL0.</span><span class="sxs-lookup"><span data-stu-id="55d86-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="55d86-121">Anche se la modalità kernel di VTL0 è compromessa da malware, non avrà accesso alle pagine del processo IUM.</span><span class="sxs-lookup"><span data-stu-id="55d86-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="55d86-122">Con VSM abilitato, l'ambiente di autorità di sicurezza locale (LSASS) viene eseguito come trustlet.</span><span class="sxs-lookup"><span data-stu-id="55d86-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="55d86-123">LSASS gestisce i criteri del sistema locale, l'autenticazione utente e il controllo gestendo i dati di sicurezza sensibili, ad esempio gli hash delle password e le chiavi Kerberos.</span><span class="sxs-lookup"><span data-stu-id="55d86-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="55d86-124">Per sfruttare i vantaggi di sicurezza di VSM, un trustlet denominato LSAISO.exe (LSA isolated) viene eseguito in VTL1 e comunica con LSASS.exe in esecuzione in VTL0 tramite un canale RPC.</span><span class="sxs-lookup"><span data-stu-id="55d86-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="55d86-125">I segreti LSAISO vengono crittografati prima di inviarli a LSASS eseguito in modalità normale VSM e le pagine di LSAISO sono protette da codice dannoso in esecuzione in VTL0.</span><span class="sxs-lookup"><span data-stu-id="55d86-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="55d86-126">**Diagramma 2: progettazione Trustlet LSASS**</span><span class="sxs-lookup"><span data-stu-id="55d86-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="55d86-127">diagramma 2: progettazione trustlet Lsass</span><span class="sxs-lookup"><span data-stu-id="55d86-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="55d86-128">Implicazioni IUM (isolated User Mode)</span><span class="sxs-lookup"><span data-stu-id="55d86-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="55d86-129">Non è possibile connettersi a un processo IUM, impedendo la possibilità di eseguire il debug del codice VTL1.</span><span class="sxs-lookup"><span data-stu-id="55d86-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="55d86-130">Questo include il debug post mortem dei dump della memoria e il fissaggio degli strumenti di debug per il debug in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="55d86-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="55d86-131">Include anche tentativi da account con privilegi o driver del kernel per caricare una DLL in un processo IUM, per inserire un thread o fornire un APC in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="55d86-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="55d86-132">Questi tentativi possono determinare la destabilizzazione dell'intero sistema.</span><span class="sxs-lookup"><span data-stu-id="55d86-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="55d86-133">Le API di Windows che potrebbero compromettere la sicurezza di un Trustlet possono non riuscire in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="55d86-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="55d86-134">Ad esempio, il caricamento di una DLL in un Trustlet lo rende disponibile in VTL0 ma non in VTL1.</span><span class="sxs-lookup"><span data-stu-id="55d86-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="55d86-135">QueueUserApc può avere esito negativo in modo invisibile all'utente se il thread di destinazione si trova in un Trustlet.</span><span class="sxs-lookup"><span data-stu-id="55d86-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="55d86-136">Anche le altre API, ad esempio CreateRemoteThread, VirtualAllocEx e Read/WriteProcessMemory, non funzioneranno come previsto quando vengono usate in Trustlets.</span><span class="sxs-lookup"><span data-stu-id="55d86-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="55d86-137">Usare il codice di esempio seguente per evitare di chiamare funzioni che tentano di aggiungere o inserire codice in un processo IUM.</span><span class="sxs-lookup"><span data-stu-id="55d86-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="55d86-138">Sono inclusi i driver del kernel che accodano APC per l'esecuzione del codice in un trustlet.</span><span class="sxs-lookup"><span data-stu-id="55d86-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d86-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d86-139">Remarks</span></span>

<span data-ttu-id="55d86-140">Se lo stato di restituzione di IsSecureProcess è Success, esaminare il \_ parametro out di SecureProcess \_ per determinare se il processo è un processo IUM.</span><span class="sxs-lookup"><span data-stu-id="55d86-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="55d86-141">I processi IUM sono contrassegnati dal sistema come "processi protetti".</span><span class="sxs-lookup"><span data-stu-id="55d86-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="55d86-142">Un risultato booleano TRUE indica che il processo di destinazione è di tipo IUM.</span><span class="sxs-lookup"><span data-stu-id="55d86-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



<span data-ttu-id="55d86-143">WDK per Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", contiene la definizione richiesta della \_ struttura di informazioni di base estesa del processo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="55d86-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="55d86-144">La versione aggiornata della struttura è definita in ntddk. h con il nuovo campo IsSecureProcess.</span><span class="sxs-lookup"><span data-stu-id="55d86-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



