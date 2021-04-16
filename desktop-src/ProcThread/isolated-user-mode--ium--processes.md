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
# <a name="isolated-user-mode-ium-processes"></a>Processi IUM (isolated User Mode)

In Windows 10 è stata introdotta una nuova funzionalità di sicurezza denominata Virtual Secure Mode (VSM). VSM sfrutta l'hypervisor Hyper-V e la modalità stecca (Second Level Address Translation) per creare un set di modalità denominate Virtual Trust Levels (VTLs). Questa nuova architettura software crea un limite di sicurezza per impedire che i processi in esecuzione in un VTL accedano alla memoria di un altro VTL. Il vantaggio di questo isolamento include la mitigazione aggiuntiva dagli exploit del kernel, proteggendo al tempo stesso gli asset, ad esempio gli hash delle password e le chiavi Kerberos.

Il diagramma 1 illustra il modello tradizionale di modalità kernel e il codice in modalità utente in esecuzione rispettivamente nell'anello 0 e nell'anello 3 della CPU. In questo nuovo modello, il codice in esecuzione nel modello tradizionale viene eseguito in VTL0 e non può accedere al VTL1 con privilegi più elevati, in cui il kernel protetto e la modalità utente isolata (IUM) eseguono codice. VTLs sono gerarchie significative che il codice in esecuzione in VTL1 è più privilegiato del codice in esecuzione in VTL0.

L'isolamento VTL viene creato dall'hypervisor di Hyper-V che assegna memoria in fase di avvio usando la conversione degli indirizzi di secondo livello. Continua in modo dinamico durante l'esecuzione del sistema, proteggendo la memoria, il kernel protetto specifica la necessità di protezione da VTL0 perché verrà usato per contenere segreti. Quando vengono allocati blocchi di memoria separati per due VTLs, viene creato un ambiente di runtime sicuro per VTL1 assegnando blocchi di memoria esclusivi a VTL1 e VTL0 con le autorizzazioni di accesso appropriate.

**Diagramma 1-architettura IUM**

![diagramma 1-architettura IUM](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Trustlets (noti anche come processi attendibili, processi protetti o processi IUM) sono programmi in esecuzione come processi IUM in VSM. Completano le chiamate di sistema eseguendone il marshalling nel kernel di Windows in esecuzione in VTL0 ring 0. VSM crea un ambiente di esecuzione ridotto che include il kernel sicuro piccolo in esecuzione in VTL1 (isolato dal kernel e dai driver in esecuzione in VTL0). Il vantaggio di sicurezza è l'isolamento delle pagine della modalità utente trustlet in VTL1 dai driver in esecuzione nel kernel VTL0. Anche se la modalità kernel di VTL0 è compromessa da malware, non avrà accesso alle pagine del processo IUM.

Con VSM abilitato, l'ambiente di autorità di sicurezza locale (LSASS) viene eseguito come trustlet. LSASS gestisce i criteri del sistema locale, l'autenticazione utente e il controllo gestendo i dati di sicurezza sensibili, ad esempio gli hash delle password e le chiavi Kerberos. Per sfruttare i vantaggi di sicurezza di VSM, un trustlet denominato LSAISO.exe (LSA isolated) viene eseguito in VTL1 e comunica con LSASS.exe in esecuzione in VTL0 tramite un canale RPC. I segreti LSAISO vengono crittografati prima di inviarli a LSASS eseguito in modalità normale VSM e le pagine di LSAISO sono protette da codice dannoso in esecuzione in VTL0.

**Diagramma 2: progettazione Trustlet LSASS**

![diagramma 2: progettazione trustlet Lsass ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implicazioni IUM (isolated User Mode)

Non è possibile connettersi a un processo IUM, impedendo la possibilità di eseguire il debug del codice VTL1. Questo include il debug post mortem dei dump della memoria e il fissaggio degli strumenti di debug per il debug in tempo reale. Include anche tentativi da account con privilegi o driver del kernel per caricare una DLL in un processo IUM, per inserire un thread o fornire un APC in modalità utente. Questi tentativi possono determinare la destabilizzazione dell'intero sistema. Le API di Windows che potrebbero compromettere la sicurezza di un Trustlet possono non riuscire in modo imprevisto. Ad esempio, il caricamento di una DLL in un Trustlet lo rende disponibile in VTL0 ma non in VTL1. QueueUserApc può avere esito negativo in modo invisibile all'utente se il thread di destinazione si trova in un Trustlet. Anche le altre API, ad esempio CreateRemoteThread, VirtualAllocEx e Read/WriteProcessMemory, non funzioneranno come previsto quando vengono usate in Trustlets.

Usare il codice di esempio seguente per evitare di chiamare funzioni che tentano di aggiungere o inserire codice in un processo IUM. Sono inclusi i driver del kernel che accodano APC per l'esecuzione del codice in un trustlet.

## <a name="remarks"></a>Commenti

Se lo stato di restituzione di IsSecureProcess è Success, esaminare il \_ parametro out di SecureProcess \_ per determinare se il processo è un processo IUM. I processi IUM sono contrassegnati dal sistema come "processi protetti". Un risultato booleano TRUE indica che il processo di destinazione è di tipo IUM.


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



WDK per Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", contiene la definizione richiesta della \_ struttura di informazioni di base estesa del processo \_ \_ . La versione aggiornata della struttura è definita in ntddk. h con il nuovo campo IsSecureProcess.


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



 

 



