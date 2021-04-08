---
description: Si noti che questo argomento si applica solo a Windows Server 2003 R2 e Windows Server 2003 con Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Backup e ripristino dello stato del sistema in Windows Server 2003 R2 e Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968489"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Backup e ripristino dello stato del sistema in Windows Server 2003 R2 e Windows Server 2003 SP1

> [!Note]  
> Questo argomento si applica solo a Windows Server 2003 R2 e Windows Server 2003 con Service Pack 1 (SP1). Per informazioni su altre versioni del sistema operativo, vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md).

 

> [!Note]  
> Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni). Per informazioni sull'uso di API e procedure fornite da Microsoft per implementare il ripristino dello stato del sistema online, vedere le risorse della community disponibili in [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

Quando si esegue un backup o un ripristino VSS, lo stato del sistema Windows viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre gestiti da operazioni di backup e ripristino come unità.

In Windows Server 2003 R2 e Windows Server 2003 con SP1, non è disponibile alcuna API Windows progettata per trattare questi oggetti come uno, quindi è consigliabile che i richiedenti dispongano di un proprio oggetto stato del sistema in modo da poter elaborare questi componenti in modo coerente.

Poiché VSS viene eseguito nelle versioni di Windows in cui la [*protezione dei file di sistema*](vssgloss-s.md) (WFP) protegge i file di stato del sistema dal danneggiamento, sono necessari passaggi speciali per eseguire il backup e il ripristino dello stato del sistema.

Lo stato del sistema è costituito dagli elementi seguenti:

-   Tutti i file protetti da WFP, i file di avvio, tra cui NTLDR, Ntdetect e le configurazioni dei contatori delle prestazioni
-   Il Active Directory (ADSI) (nei sistemi che sono controller di dominio)
-   Cartella del volume di sistema (SYSVOL) replicata dal servizio Replica file (FRS) (nei sistemi che sono controller di dominio)
-   Server di certificazione (nei sistemi che forniscono autorità di certificazione)
-   Database cluster (nei sistemi che costituiscono un nodo di un cluster Windows)
-   Servizio Registro di sistema
-   Database di registrazione della classe COM+

È possibile eseguire il backup dello stato del sistema in qualsiasi ordine.

Tuttavia, il ripristino dello stato del sistema dovrebbe sostituire prima i file di avvio ed eseguire il commit della sezione di sistema (hive) del registro di sistema come passaggio finale del processo e potrebbe verificarsi nell'ordine seguente:

1.  Ripristinare i file di avvio.
2.  Database di registrazione della classe COM+
3.  Ripristinare SYSVOL, server dei certificati e database cluster (se necessario).
4.  Ripristinare Active Directory (se necessario).
5.  Ripristinare il registro di sistema.

Alcuni servizi di sistema, ad esempio l'autorità di certificazione, hanno writer VSS convenzionali e seguono gli algoritmi di backup e ripristino VSS. Altri, ad esempio il registro di sistema, richiedono operazioni di backup o ripristino personalizzate. per altre informazioni, vedere [backup e ripristini personalizzati](custom-backups-and-restores.md).

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>Backup e ripristini VSS dei file di avvio e di sistema

È necessario eseguire il backup e il ripristino dei file di avvio e di sistema solo come singola entità.

Un richiedente può utilizzare in modo sicuro versioni di questi file con copia shadow e verificare che il volume di sistema e il dispositivo di avvio siano [*copiati*](vssgloss-s.md).

I file di sistema e di avvio includono:

-   I file di avvio principali: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (se presente)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> % SystemRoot% \\ system32 \\ Catroot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   Tutti i file protetti dalla [*protezione dei file di sistema*](vssgloss-s.md) ed enumerati da [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (vedere operazioni di ripristino VSS dei file protetti con WFP) -   i file di configurazione del contatore delle prestazioni: <dl> % SystemRoot% \\ system32 \\ ? 00?. dat  
    % SystemRoot% \\ system32 \\ ? 00?. bak </dl>
-   Se presente, il file della metabase di Internet Information Server (IIS) deve essere incluso nelle operazioni di backup e ripristino perché contiene lo stato utilizzato da Microsoft Exchange e altre applicazioni di rete. Questo file è disponibile nel percorso: <dl> % SystemRoot% \\ system32 \\ inetsrv \\ metabase. bin </dl>
-   Se viene eseguito il backup del file della metabase IIS, le chiavi per consentire alle applicazioni di leggere determinate voci crittografate devono essere ripristinate come parte dello stato del sistema. I file sono disponibili in: <dl> % SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*  
    % AllUsersProfile% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\* </dl>
-Quando si esegue il backup dei file di avvio e di sistema, potrebbe essere necessario determinare il dispositivo di avvio DOS eseguendo le operazioni seguenti: 1. trovare la partizione di sistema in **HKEY \_ Local \_ Machine** \\ **System** \\ **Setup** \\ **SYSTEMPARTITION**.
    2.  Passare la variabile di ambiente radice del sistema (% SystemRoot%) al gestore del montaggio per ottenere il nome del dispositivo NT.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>Operazioni di ripristino VSS dei file protetti da WFP

Il servizio WFP è progettato per impedire la sostituzione accidentale o a fasi dei file di sistema. Pertanto, è necessario eseguire passaggi speciali per ripristinare i dati di WFP.

Indica che il writer del servizio Copia Shadow del volume deve specificare il **\_ ripristino VSS RME \_ \_ al \_** Metodo Restore del ripristino durante la definizione del documento di metadati del writer. Se un richiedente determina che il writer del Pam non è stato in grado di specificare questo metodo di ripristino, significa che si è verificato un errore del writer.

Un richiedente deve implementare un metodo Restore **del \_ ripristino VSS RME \_ \_ al \_ riavvio** usando la funzione Win32 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) con il **ritardo MOVEFILE fino al parametro \_ \_ \_ reboot** per sostituire i file di sistema. I file ripristinati non vengono copiati nelle directory effettive dei file di sistema fino al riavvio del sistema. La sovrascrittura dei file di sistema protetti verrà eseguita solo se il valore della voce **reg \_ Word** del registro di sistema seguente è impostato su 1:

**HKEY \_ \_** \\  \\ Gestore sessioni **CurrentControlSet** controllo di sistema del computer locale \\  \\  \\ **AllowProtectedRenames** = 1

Questo valore deve essere impostato prima di qualsiasi avvio in cui i file protetti devono essere sostituiti tramite [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e viene eliminato dopo il riavvio.

È necessario eseguire il backup o il ripristino della directory dllcache di sistema, con backup e ripristino del volume di avvio, ed esaminando la voce del registro di sistema **reg \_ expand \_ SZ** :

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ Espandi \_ SZ</dd> </dl>

Il contenuto della directory dllcache di sistema viene ricompilato tramite il controllo file di sistema (SFC) dal prompt dei comandi:

-   L'opzione **/scanonce** analizza tutti i file protetti all'avvio del sistema successivo.
-   L'opzione **/scannow** analizza immediatamente tutti i file protetti.

Tutti i file protetti verranno analizzati e tutte le versioni non valide verranno sostituite nella directory e nel percorso dllcache.

Sono presenti quattro file che fanno parte del WFP che non possono essere ripristinati con i file WFP:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Questi file consentono di ripristinare i file del WFP e, di conseguenza, esiste una dipendenza circolare. Attualmente, non è possibile ripristinare questi file tranne che per reinstallare Windows.

 

 
