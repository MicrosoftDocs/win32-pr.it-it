---
description: Nota Questo argomento si applica solo Windows Server 2003 R2 e Windows Server 2003 con Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Backup e ripristino dello stato del sistema in Windows Server 2003 R2 e Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4803acc5981cc74084789064bd276baa28b35c0ffe225e49d2b65ba5485e51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032951"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Backup e ripristino dello stato del sistema in Windows Server 2003 R2 e Windows Server 2003 SP1

> [!Note]  
> Questo argomento si applica solo Windows Server 2003 R2 e Windows Server 2003 con Service Pack 1 (SP1). Per informazioni sulle altre versioni del sistema operativo, vedere [Backup e ripristino dello stato del sistema.](locating-additional-system-files.md)

 

> [!Note]  
> Microsoft non offre supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online Windows (tutte le versioni). Per informazioni sull'uso delle API e delle procedure fornite da Microsoft per implementare ripristini online dello stato del sistema, vedere le risorse della community disponibili in [MSDN Community Center.](https://msdn.microsoft.com/community/default.aspx)

 

Quando si esegue un backup o un ripristino vss, lo stato Windows sistema viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.

In Windows Server 2003 R2 e Windows Server 2003 con SP1 non esiste alcuna API Windows progettata per considerare questi oggetti come uno, pertanto è consigliabile che i richiedenti dispongono di un proprio oggetto stato del sistema in modo che possano elaborare questi componenti in modo coerente.

Poiché VSS viene eseguito nelle versioni di Windows in cui Protezione [*file*](vssgloss-s.md) di sistema protegge i file dello stato del sistema dal danneggiamento, sono necessari passaggi speciali per eseguire il backup e il ripristino dello stato del sistema.

Lo stato del sistema è costituito dai seguenti elementi:

-   Tutti i file protetti da WFP, i file di avvio inclusi ntldr, ntdetect e le configurazioni dei contatori delle prestazioni
-   Active Directory (ADSI) (nei sistemi che sono controller di dominio)
-   Cartella del volume di sistema (SYSVOL) replicata dal servizio Replica file (FRS) (nei sistemi che sono controller di dominio)
-   Server dei certificati (nei sistemi che forniscono l'autorità di certificazione)
-   Database del cluster (nei sistemi che sono un nodo di un cluster Windows cluster)
-   Servizio Registro di sistema
-   Database di registrazione della classe COM+

È possibile eseguire il backup dello stato del sistema in qualsiasi ordine.

Tuttavia, il ripristino dello stato del sistema deve sostituire prima i file di avvio ed eseguire il commit della sezione di sistema (hive) del Registro di sistema come passaggio finale del processo e potrebbe verificarsi nell'ordine seguente:

1.  Ripristinare i file di avvio.
2.  Database di registrazione della classe COM+
3.  Ripristinare i database SYSVOL, Server certificati e Cluster (se necessario).
4.  Ripristinare Active Directory (se necessario).
5.  Ripristinare il Registro di sistema.

Alcuni servizi di sistema, ad esempio l'autorità di certificazione, dispongono di vss writer convenzionali e seguono gli algoritmi di backup e ripristino del Servizio Copia Copia Backup. Altri, ad esempio il Registro di sistema, richiedono operazioni di backup o ripristino personalizzate. Per altre informazioni, vedere [Backup e ripristini personalizzati.](custom-backups-and-restores.md)

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>Backup e ripristini vss di file di avvio e di sistema

I file di avvio e di sistema devono essere sottoposti a backup e ripristinati solo come singola entità.

Un richiedente può usare in modo sicuro le versioni copiate shadow di questi file e deve assicurarsi che il volume di sistema e il dispositivo di avvio siano [*copiati in modo shadow.*](vssgloss-s.md)

I file di sistema e di avvio includono:

-   I file di avvio principali: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (se presente)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> %SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   Tutti i file protetti da Protezione [*file*](vssgloss-s.md) di sistema ed enumerati da [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (vedere Operazioni di ripristino VSS di file protetti da WFP) File di configurazione del contatore -   delle prestazioni: <dl> %SystemRoot% \\ System32 \\ Perf?00?. Dat  
    %SystemRoot% \\ System32 \\ Perf?00?. Bak </dl>
-Se presente, il file della metabase di Internet Information Server (IIS) deve essere incluso nelle operazioni di backup e ripristino perché contiene lo stato utilizzato da Microsoft Exchange e altre applicazioni di rete. Questo file è disponibile nel percorso: <dl> %SystemRoot% \\ System32 \\ InetSrv \\ Metabase.bin </dl>
-   Se viene eseguito il backup del file della metabase IIS, le chiavi per consentire alle applicazioni di leggere determinate voci crittografate devono essere ripristinate come parte dello stato del sistema. I file sono disponibili in: <dl> %SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
    %AllUsersProfile% \\ Microsoft Crypto RSA \\ \\ \\ MachineKeys\\\* </dl>
-Quando si esegue il backup dei file di avvio e di sistema, può risultare necessario determinare il dispositivo di avvio DOS eseguendo le operazioni seguenti: Trovare la partizione di sistema 1. in **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **Setup** \\ **SystemPartition**.
    2.  Passare la variabile di ambiente System Root (%SystemRoot%) alla gestione del montaggio per ottenere il nome del dispositivo NT.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>Operazioni di ripristino VSS di file protetti da PAM

Il servizio WFP è progettato per impedire la sostituzione accidentale o a partizionate dei file di sistema. Pertanto, è necessario eseguire passaggi speciali per ripristinare i dati WFP.

Indica che il writer PAM deve specificare il metodo di ripristino **RME DI VSS \_ al \_ \_ \_ riavvio** durante la definizione del documento di metadati del writer. Se un richiedente determina che il writer PAM non è riuscito a specificare questo metodo di ripristino, indica un errore del writer.

Un richiedente deve implementare un metodo di ripristino di **VSS \_ RME \_ RESTORE \_ \_ al** riavvio usando la funzione [**Win32 MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) con il **parametro MOVEFILE DELAY UNTIL \_ \_ \_ REBOOT** per sostituire i file di sistema. I file ripristinati non vengono copiati nelle directory dei file di sistema effettive fino al riavvio del sistema. La sovrascrittura dei file di sistema protetti si verificherà solo se il valore della voce del Registro di sistema **\_ REG WORD** seguente è impostato su 1:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **AllowProtectedRenames** = 1

Questo valore deve essere impostato prima di qualsiasi avvio in cui i file protetti devono essere sostituiti tramite [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e viene eliminato dopo il riavvio.

È anche necessario eseguire il backup o il ripristino della directory dllcache di sistema, con backup e ripristino del volume di avvio, e si trova esaminando la voce del Registro di sistema **REG \_ EXPAND \_ SZ:**

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ EXPAND \_ SZ</dd> </dl>

Il contenuto della directory dllcache di sistema viene ricompilato usando il Verifica file di sistema (SFC) dal prompt dei comandi:

-   **L'opzione /SCANONCE** analizza tutti i file protetti al successivo avvio del sistema.
-   **L'opzione /SCANNOW** analizza immediatamente tutti i file protetti.

Tutti i file protetti verranno analizzati e tutte le versioni non valide verranno sostituite sia nella directory che nel percorso dllcache.

Esistono quattro file che fanno parte del file WFP che non possono essere ripristinati con i file WFP:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Questi file sono utili nel processo di ripristino dei file WFP e, di conseguenza, esiste una dipendenza circolare. Attualmente, non è possibile ripristinare questi file se non reinstallarli Windows.

 

 
