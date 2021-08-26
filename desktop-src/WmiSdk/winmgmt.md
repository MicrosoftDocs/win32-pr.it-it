---
description: Winmgmt è il servizio WMI all'interno del processo SVCHOST in esecuzione nel &\# 0034; LocalSystem&\# account 0034;.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: Winmgmt
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
ms.openlocfilehash: d28d37faf454accd91281034d0aeb8df5e10dddb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879866"
---
# <a name="winmgmt"></a>Winmgmt

Winmgmt è il servizio WMI all'interno del processo SVCHOST in esecuzione con l'account "LocalSystem".

In tutti i casi, il servizio WMI viene avviato automaticamente quando la prima applicazione di gestione o script richiede la connessione a uno spazio dei nomi WMI. Per altre informazioni, vedere [Avvio e arresto del servizio WMI](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> WMI è un componente di base del Windows operativo che consente agli sviluppatori e agli amministratori IT di scrivere script e applicazioni per automatizzare determinate attività. Winmgmt.exe è il servizio che consente l'esecuzione di WMI nel computer locale. Per altre informazioni sull'uso di WMI, vedere [Uso di WMI.](using-wmi.md) Se è stato ricevuto un messaggio di errore relativo winmgmt.exe, vedere [Risoluzione dei problemi wmi.](wmi-troubleshooting.md) Per altre informazioni sull'Winmgmt.exe, vedere [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

Quando viene eseguito dal prompt dei comandi, il servizio WMI dispone delle opzioni seguenti.

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

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup** *&lt; filename &gt;* 
</dt> <dd>

Consente a WMI di eseguire il backup del repository con il nome file specificato. *L'argomento filename* deve contenere il percorso completo del file. Questo processo richiede un blocco di scrittura sul repository in modo che le operazioni di scrittura nel repository siano sospese fino al completamento del processo di backup.

Se non si specifica un percorso per il file, viene inserito nella directory %Windir% \\ System32.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore filename** *&lt; &gt;* *&lt; flag &gt;* 
</dt> <dd>

Ripristina manualmente il repository WMI dal file di backup specificato. *L'argomento filename* deve contenere il percorso completo del file di backup. Per eseguire l'operazione di ripristino, WMI salva il repository esistente per eseguire il write back se l'operazione non riesce. Il repository viene quindi ripristinato dal file di backup specificato nell'argomento *filename.* Se non è possibile ottenere l'accesso esclusivo al repository, i client esistenti vengono disconnessi da WMI.

*L'argomento flag* deve essere 1 (forza la disconnessione degli utenti e il ripristino) o 0 (ripristino predefinito se nessun utente connesso) e specifica la modalità di ripristino.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *&lt; winmgmt-service-process-id &gt;* 
</dt> <dd>

Registra le librerie delle prestazioni del computer con WMI. PID WMI è l'ID del processo per il servizio WMI.

Necessario solo se le classi di monitoraggio delle prestazioni non restituiscono risultati affidabili.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[ *&lt; level &gt;*\]
</dt> <dd>

Sposta il servizio Winmgmt in un processo Svchost autonomo con un endpoint DCOM fisso. L'endpoint predefinito è "ncacn \_ ip \_ tcp.0.24158". Tuttavia, l'endpoint può essere modificato eseguendo Dcomcnfg.exe. Per altre informazioni sulla configurazione di una porta fissa per WMI, vedere [Impostazione di una porta fissa per WMI.](setting-up-a-fixed-port-for-wmi.md)

*L'argomento level* è il livello di autenticazione per il processo Svchost. WMI viene in genere eseguito come parte di un host del servizio condiviso e non è possibile aumentare il livello di autenticazione solo per WMI. Se *level* non viene specificato, il valore predefinito è 4 (**RPC C \_ \_ AUTHN \_ LEVEL \_ PKT** o **WbemAuthenticationLevelPkt**).

È possibile eseguire WMI in modo più sicuro aumentando il livello di autenticazione a Packet Privacy (**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** o **WbemAuthenticationLevelPktPrivacy**). I livelli di autenticazione per Visual Basic script sono descritti in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum). Per C++, vedere [Impostazione del livello di sicurezza del processo predefinito tramite C++.](setting-the-default-process-security-level-using-c-.md) Per altre informazioni, vedere [Gestione della sicurezza WMI.](maintaining-wmi-security.md)

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Sposta il servizio Winmgmt nel processo Svchost condiviso.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository** *&lt; path &gt;* 
</dt> <dd>

Esegue una verifica coerenza nel repository WMI. Quando si aggiunge **l'opzione /verifyrepository** senza l'argomento *&lt; path, &gt;* viene verificato il repository live attualmente usato da WMI. Quando si specifica *l'argomento path,* è possibile verificare qualsiasi copia salvata del repository. In questo caso, l'argomento path deve contenere il percorso completo della copia del repository salvata. Il repository salvato deve essere una copia dell'intera cartella del repository. Per altre informazioni sugli errori restituiti da questo comando, vedere la sezione Osservazioni.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Esegue una verifica coerenza nel repository WMI e, se viene rilevata un'incoerenza, ricompila il repository. Il contenuto del repository incoerente viene unito nel repository ricompilato, se può essere letto. L'operazione di recupero funziona sempre con il repository attualmente in uso dal servizio WMI. Per altre informazioni sugli errori restituiti da questo comando, vedere la sezione Osservazioni.

% file MOF che contengono l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) vengono ripristinati nel repository.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

Il repository viene reimpostato sullo stato iniziale quando il sistema operativo viene installato per la prima volta. I file MOF che contengono l'istruzione del preprocessore [**\# pragma autorecover**](pragma-autorecover.md) vengono ripristinati nel repository.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo strumento si trova nella directory %Windir% \\ System32 \\ wbem. Per un elenco delle opzioni disponibili, digitare `WinMgmt /?` al prompt dei comandi.

Il repository WMI, noto anche come repository CIM, non è solo un singolo file, ma una raccolta di file all'interno della cartella Repository che funzionano insieme come database. Quando si usa **l'opzione /backup** per eseguire il backup del repository, il backup risultante è un singolo file compresso.

WMI restituisce l'errore **ERROR \_ INTERNAL DB \_ \_ CORRUPTION** (net helpmsg 1358) se un'operazione di verifica indica che il repository non è in uno stato coerente. Questo errore può essere restituito da qualsiasi comando che esegue la verifica del repository, ad esempio **/verifyrepository** **o /salvagerepository.**

> [!Note]
>
> Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono avere origine in altre parti del sistema operativo e emergono come errori tramite WMI. In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.
>
> Per altre informazioni sull'origine del problema, scaricare ed eseguire lo strumento [Utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) della riga di comando di diagnostica. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report aiuta anche i servizi di supporto Tecnico Microsoft a fornire assistenza. È possibile scaricare il [Utilità di diagnosi di WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Risoluzione dei problemi wmi](wmi-troubleshooting.md)
</dt> <dt>

[Connessione a WMI in modalità remota a partire da Vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

