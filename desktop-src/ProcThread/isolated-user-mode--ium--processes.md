---
description: Windows 10 stata introdotta una nuova funzionalità di sicurezza denominata Modalità protetta virtuale (VSM).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Processi IUM (Isolated User Mode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982d9924f60d02a74aa7237e5c3bb16e787f1d3a0cc07e9693e9cd47335cedc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032542"
---
# <a name="isolated-user-mode-ium-processes"></a>Processi IUM (Isolated User Mode)

Windows 10 stata introdotta una nuova funzionalità di sicurezza denominata Modalità protetta virtuale (VSM). VSM sfrutta hypervisor Hyper-V e SLAT (Second Level Address Translation) per creare un set di modalità denominate livelli di attendibilità virtuale (VCL). Questa nuova architettura software crea un limite di sicurezza per impedire ai processi in esecuzione in una VTL di accedere alla memoria di un altro VTL. Il vantaggio di questo isolamento include una mitigazione aggiuntiva degli exploit del kernel, proteggendo al tempo stesso asset come hash delle password e chiavi Kerberos.

Il diagramma 1 illustra il modello tradizionale di modalità kernel e codice in modalità utente in esecuzione rispettivamente nell'anello CPU 0 e nell'anello 3. In questo nuovo modello, il codice in esecuzione nel modello tradizionale viene eseguito in VTL0 e non può accedere alla VTL1 con privilegi più elevati, in cui il kernel protetto e la modalità utente isolato (IUM) eseguono codice. I VTL sono gerarchici, vale a dire che qualsiasi codice in esecuzione in VTL1 ha più privilegi rispetto al codice in esecuzione in VTL0.

L'isolamento VTL viene creato dall'hypervisor Hyper-V che assegna memoria in fase di avvio usando slat (Second Level Address Translation). Continua in modo dinamico durante l'esecuzione del sistema, proteggendo la memoria specificata dal kernel protetto che deve essere protetta da VTL0 perché verrà usata per contenere segreti. Quando vengono allocati blocchi di memoria separati per i due VTL, viene creato un ambiente di runtime sicuro per VTL1 assegnando blocchi di memoria esclusivi a VTL1 e VTL0 con le autorizzazioni di accesso appropriate.

**Diagramma 1 - Architettura IUM**

![diagramma 1 - Architettura ium](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlet

I trustlet (noti anche come processi attendibili, processi protetti o processi IUM) sono programmi in esecuzione come processi IUM in VSM. Completano le chiamate di sistema eseguendo il marshalling al kernel Windows in esecuzione nell'anello VTL0 0. VSM crea un ambiente di esecuzione di piccole dimensioni che include il piccolo kernel protetto in esecuzione in VTL1 (isolato dal kernel e dai driver in esecuzione in VTL0). Il vantaggio di sicurezza chiaro è l'isolamento delle pagine in modalità utente trustlet in VTL1 dai driver in esecuzione nel kernel VTL0. Anche se la modalità kernel di VTL0 è compromessa da malware, non avrà accesso alle pagine del processo IUM.

Con VSM abilitato, l'ambiente Autorità di sicurezza locale (LSASS) viene eseguito come trustlet. LSASS gestisce i criteri di sistema locali, l'autenticazione utente e il controllo durante la gestione dei dati di sicurezza sensibili, ad esempio hash delle password e chiavi Kerberos. Per sfruttare i vantaggi della sicurezza di VSM, un trustlet denominato LSAISO.exe (isolato LSA) viene eseguito in VTL1 e comunica con LSASS.exe in esecuzione in VTL0 tramite un canale RPC. I segreti LSAISO vengono crittografati prima di inviarli a LSASS in esecuzione in modalità normale VSM e le pagine di LSAISO sono protette da codice dannoso in esecuzione in VTL0.

**Diagramma 2 - Progettazione trustlet LSASS**

![diagramma 2 : progettazione trustlet lsass ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implicazioni della modalità utente isolata (IUM)

Non è possibile connettersi a un processo IUM, inibendo la possibilità di eseguire il debug del codice VTL1. Sono inclusi il debug post-mortem dei dump di memoria e il collegamento degli strumenti di debug per il debug in tempo reale. Include anche i tentativi da parte di account con privilegi o driver del kernel di caricare una DLL in un processo IUM, inserire un thread o distribuire un APC in modalità utente. Tali tentativi possono comportare la destabilizzazione dell'intero sistema. Windows Le API che comprometterebbero la sicurezza di un trustlet potrebbero non riuscire in modo imprevisto. Ad esempio, il caricamento di una DLL in un trustlet la rende disponibile in VTL0 ma non in VTL1. QueueUserApc potrebbe non riuscire automaticamente se il thread di destinazione si trova in un trustlet. Anche altre API, ad esempio CreateRemoteThread, VirtualAllocEx e Read/WriteProcessMemory, non funzioneranno come previsto quando vengono usate nei trustlet.

Usare il codice di esempio seguente per impedire la chiamata di funzioni che tentano di collegare o inserire codice in un processo IUM. Sono inclusi i driver del kernel che accodono le API per l'esecuzione di codice in un trustlet.

## <a name="remarks"></a>Commenti

Se lo stato restituito di IsSecureProcess è riuscito, esaminare il parametro SecureProcess Out per determinare se il \_ processo è un processo \_ IUM. I processi IUM sono contrassegnati dal sistema come "Processi sicuri". Un risultato booleano TRUE indica che il processo di destinazione è di tipo IUM.


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



WdK per Windows 10, "Windows Driver Kit - Windows 10.0.15063.0", contiene la definizione richiesta della struttura PROCESS \_ EXTENDED \_ BASIC \_ INFORMATION. La versione aggiornata della struttura è definita in ntddk.h con il nuovo campo IsSecureProcess.


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



 

 



