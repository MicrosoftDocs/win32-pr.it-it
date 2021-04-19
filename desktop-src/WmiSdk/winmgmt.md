---
description: WinMgmt è il servizio WMI all'interno del processo SVCHOST in esecuzione nel &\# 0034; LocalSystem&\# 0034; account.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318170"
---
# <a name="winmgmt"></a>winmgmt

WinMgmt è il servizio WMI all'interno del processo SVCHOST in esecuzione con l'account "LocalSystem".

In tutti i casi, il servizio WMI viene avviato automaticamente quando il primo script o un'applicazione di gestione richiede la connessione a uno spazio dei nomi WMI. Per altre informazioni, vedere [Avvio e arresto del servizio WMI](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> WMI è un componente fondamentale del sistema operativo Windows che consente agli sviluppatori e agli amministratori IT di scrivere script e applicazioni per automatizzare determinate attività. Winmgmt.exe è il servizio che consente l'esecuzione di WMI nel computer locale. Per ulteriori informazioni sull'utilizzo di WMI, vedere [utilizzo di WMI](using-wmi.md). Se è stato ricevuto un messaggio di errore relativo winmgmt.exe, vedere la pagina relativa alla [risoluzione dei problemi di WMI](wmi-troubleshooting.md). Per ulteriori informazioni su Winmgmt.exe, vedere [utilizzo degli strumenti di gestione WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

Quando viene eseguito dal prompt dei comandi, il servizio WMI presenta le opzioni seguenti.

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a>Commutatori

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup***<filename>* 
</dt> <dd>

Fa in modo che WMI Esegui il backup del repository nel nome file specificato. L'argomento *filename* deve contenere il percorso completo del percorso del file. Questo processo richiede un blocco di scrittura nel repository, in modo che le operazioni di scrittura nel repository vengano sospese fino al completamento del processo di backup.

Se non si specifica un percorso per il file, questo viene inserito nella directory% windir% \\ system32.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>**<flag>* 
</dt> <dd>

Ripristina manualmente il repository WMI dal file di backup specificato. L'argomento *filename* deve contenere il percorso completo del percorso del file di backup. Per eseguire l'operazione di ripristino, WMI Salva il repository esistente per eseguire il writeback se l'operazione ha esito negativo. Il repository viene quindi ripristinato dal file di backup specificato nell'argomento *filename* . Se non è possibile ottenere l'accesso esclusivo al repository, i client esistenti vengono disconnessi da WMI.

Il *flag* argument deve essere 1 (Force Disconnect Users and Restore) o 0 (ripristino predefinito se nessun utente connesso) e specifica la modalità di ripristino.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<WinMgmt-Service-process-ID>* 
</dt> <dd>

Registra le librerie di prestazioni del computer con WMI. Il PID WMI è l'ID del processo per il servizio WMI.

Necessaria solo se le classi di performance monitor non restituiscono risultati affidabili.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]
</dt> <dd>

Sposta il servizio WinMgmt in un processo Svchost autonomo con un endpoint DCOM fisso. L'endpoint predefinito è "ncacn \_ IP \_ TCP. 0.24158". Tuttavia, l'endpoint può essere modificato eseguendo Dcomcnfg.exe. Per ulteriori informazioni sulla configurazione di una porta fissa per WMI, vedere la pagina [relativa alla configurazione di una porta fissa per WMI](setting-up-a-fixed-port-for-wmi.md).

L'argomento *Level* è il livello di autenticazione per il processo Svchost. WMI viene in genere eseguito come parte di un host del servizio condiviso e non è possibile aumentare il livello di autenticazione solo per WMI. Se *Level* non è specificato, il valore predefinito è 4 (**RPC \_ C Authentication \_ \_ level \_ PKT** o **WbemAuthenticationLevelPkt**).

È possibile eseguire WMI in modo più sicuro aumentando il livello di autenticazione alla privacy dei pacchetti (**RPC \_ C \_ AuthN \_ level \_ PKT \_ privacy** o **WbemAuthenticationLevelPktPrivacy**). I livelli di autenticazione per Visual Basic e scripting sono descritti in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum). Per C++, vedere [impostazione del livello di sicurezza del processo predefinito con c++](setting-the-default-process-security-level-using-c-.md). Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Sposta il servizio WinMgmt nel processo Svchost condiviso.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository***<path>* 
</dt> <dd>

Esegue una verifica di coerenza nel repository WMI. Quando si aggiunge l'opzione **/verifyrepository** senza l' *<path>* argomento, viene verificato il repository Live attualmente utilizzato da WMI. Quando si specifica l'argomento *path* , è possibile verificare qualsiasi copia salvata del repository. In questo caso, l'argomento path deve contenere il percorso completo della copia del repository salvata. Il repository salvato deve essere una copia dell'intera cartella del repository. Per ulteriori informazioni sugli errori restituiti da questo comando, vedere la sezione Osservazioni.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Esegue una verifica di coerenza sul repository WMI e, se viene rilevata un'incoerenza, ricompila il repository. Il contenuto del repository non coerente viene unito al repository ricompilato, se può essere letto. L'operazione di salvataggio funziona sempre con il repository attualmente utilizzato dal servizio WMI. Per ulteriori informazioni sugli errori restituiti da questo comando, vedere la sezione Osservazioni.

% File MOF che contengono l'istruzione del preprocessore [**\# pragma autorecupero**](pragma-autorecover.md) vengono ripristinati nel repository.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

Il repository viene reimpostato sullo stato iniziale quando viene installato per la prima volta il sistema operativo. I file MOF contenenti l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) vengono ripristinati nel repository.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo strumento si trova nella directory% windir% \\ system32 \\ WBEM. Per un elenco delle opzioni disponibili, digitare `WinMgmt /?` al prompt dei comandi.

Il repository WMI, noto anche come repository CIM, non è solo un singolo file, ma una raccolta di file all'interno della cartella del repository che operano insieme come database. Quando si usa l'opzione **/backup** per eseguire il backup del repository, il backup risultante è un singolo file compresso.

WMI restituisce il **\_ \_ \_ danneggiamento interno del database** di errore (NET HELPMSG 1358) se un'operazione di verifica indica che lo stato del repository non è coerente. Questo errore può essere restituito da qualsiasi comando che esegua la verifica del repository, ad esempio **/verifyrepository** o **/salvagerepository**.

> [!Note]
>
> Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI. In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.
>
> Per ulteriori informazioni sull'origine del problema, scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnostic. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft. È possibile scaricare il [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[Connessione a WMI in modalità remota a partire da vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

