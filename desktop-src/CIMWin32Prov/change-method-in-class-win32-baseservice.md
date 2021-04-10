---
description: Modifica un oggetto servizio derivato da Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Metodo Change della classe Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127227"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Metodo Change della classe Win32 \_ BaseService

Il metodo **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un oggetto servizio derivato da [**Win32 \_ BaseService**](win32-baseservice.md). Il [**parametro \_ LoadOrderGroup di Win32**](win32-loadordergroup.md) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, perché i servizi dipendono tra loro. Per il corretto funzionamento di questi servizi dipendenti sono necessari servizi precedenti.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DisplayName* \[ in\]
</dt> <dd>

Nome visualizzato per un servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto nella gestione controllo servizi. I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.

Constraints: accetta lo stesso valore del parametro *Name* .

Esempio: "ATDISK".

</dd> <dt>

*Nome percorso* \[ in\]
</dt> <dd>

Percorso completo del file eseguibile che implementa un servizio.

Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ in\]
</dt> <dd>

Tipo di servizi forniti ai processi che li chiamano.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver kernel** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver del file System** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver di riconoscimento** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Processo personalizzato** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo di condivisione** (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Processo interattivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ in\]
</dt> <dd>

Gravità di un errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal sistema.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignora** (0)


</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (1)


</dt> <dd>

Normale. L'utente viene notificato.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)


</dt> <dd>

Il sistema viene riavviato con l'ultima configurazione corretta.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Modalità di avvio del servizio di base di Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Avvio **avvio** ("avvio")


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema** ("sistema")


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("automatico")


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta** ("manuale")


</dt> <dd>

Servizio per avviare il gestore di controllo del servizio quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-baseservice.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** ("disabilitato")


</dt> <dd>

Servizio che non può essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

Se **true**, il servizio può creare o comunicare con una finestra sul desktop.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio, che dipende dal tipo di servizio. Il nome dell'account può essere nel formato DomainName \\ username o. \\ Nome utente. Quando viene eseguito, il processo del servizio viene registrato utilizzando uno dei due formati precedenti. Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente. Se viene specificata una stringa vuota, il servizio viene connesso come account LocalSystem. Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ad esempio \\ filesystem \\ RDR o \\ driver \\ XNS, usato dal sistema di input e output (i/O) per caricare il driver di dispositivo. Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio, ad esempio DWDOM \\ admin.

È anche possibile usare il formato del nome dell'entità utente (UPN) per specificare il nome **iniziale**, ad esempio *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ in\]
</dt> <dd>

Password per il nome dell'account specificato dal parametro *StartName* . Specificare **null** se non si modifica la password. Specificare una stringa vuota se il servizio non dispone di una password.

> [!Note]  
> Quando si modifica un servizio da sistema locale a rete o da rete a sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Nome del gruppo a cui è associato. I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza di caricamento dei servizi in un sistema operativo. Se il puntatore è **null** o punta a una stringa vuota, il servizio non appartiene a un gruppo. Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* . I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo. Il registro di sistema include un elenco di gruppi di ordini di carico situati in **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.

</dd> <dt>

*LoadOrderGroupDependencies* \[ in\]
</dt> <dd>

Elenco di gruppi di ordini di caricamento che devono essere avviati prima dell'avvio del servizio. La matrice è con doppia terminazione **null**. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*ServiceDependencies* \[ in\]
</dt> <dd>

Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. La matrice è con doppia terminazione **null**. Se il puntatore è **null** o punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.

<dl> <dt>

**Success**
</dt> <dd>

0

La richiesta è stata accettata.

</dd> <dt>

**Non supportato**
</dt> <dd>

1

La richiesta non è supportata.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

L'utente non dispone dei privilegi di accesso necessari.

</dd> <dt>

**Servizi dipendenti in esecuzione**
</dt> <dd>

3

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**Controllo del servizio non valido**
</dt> <dd>

4

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**Il servizio non può accettare il controllo**
</dt> <dd>

5

Impossibile inviare il codice di controllo richiesto al servizio perché la proprietà [**state**](win32-baseservice.md) nell'oggetto [**Win32 \_ BaseService**](win32-baseservice.md) è uguale a 0, 1 o 2.

</dd> <dt>

**Servizio non attivo**
</dt> <dd>

6

Il servizio non è stato avviato.

</dd> <dt>

**Timeout richiesta servizio**
</dt> <dd>

7

Il servizio non risponde alla richiesta di avvio rapidamente.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Processo interattivo.

</dd> <dt>

**Percorso non trovato**
</dt> <dd>

9

Impossibile trovare il percorso di directory del file eseguibile del servizio.

</dd> <dt>

**Servizio già in esecuzione**
</dt> <dd>

10

Il servizio è già in esecuzione.

</dd> <dt>

**Database del servizio bloccato**
</dt> <dd>

11

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**Dipendenza servizio eliminata**
</dt> <dd>

12

Una dipendenza per cui si basa questo servizio viene rimossa dal sistema.

</dd> <dt>

**Errore di dipendenza del servizio**
</dt> <dd>

13

Il servizio non trova il servizio necessario da un servizio dipendente.

</dd> <dt>

**Servizio disabilitato**
</dt> <dd>

14

Il servizio è disabilitato dal sistema.

</dd> <dt>

**Accesso al servizio non riuscito**
</dt> <dd>

15

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**Servizio contrassegnato per l'eliminazione**
</dt> <dd>

16

Questo servizio verrà rimosso dal sistema.

</dd> <dt>

**Servizio senza thread**
</dt> <dd>

17

Nessun thread di esecuzione per il servizio.

</dd> <dt>

**Stato dipendenza circolare**
</dt> <dd>

18

All'avvio del servizio sono state rilevate dipendenze circolari.

</dd> <dt>

**Stato nome duplicato**
</dt> <dd>

19

È presente un servizio in esecuzione con lo stesso nome.

</dd> <dt>

**Stato nome non valido**
</dt> <dd>

20

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**Stato parametro non valido**
</dt> <dd>

21

Sono stati passati parametri non validi al servizio.

</dd> <dt>

**Stato account del servizio non valido**
</dt> <dd>

22

L'account per il servizio da eseguire non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

</dd> <dt>

**Il servizio stato esiste**
</dt> <dd>

23

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**Servizio già sospeso**
</dt> <dd>

24

Il servizio è attualmente sospeso nel sistema.

</dd> <dt>

**Altri**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

Per modificare un servizio da una rete a un sistema locale, usare i valori seguenti per i parametri *StartName* e *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Per modificare un servizio da un sistema locale a una rete, usare i valori seguenti per i parametri *StartName* e *StartPassword* :


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_BaseService Win32**](win32-baseservice.md)
</dt> </dl>

 

