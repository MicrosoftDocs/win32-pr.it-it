---
description: Modifica un \_ servizio Win32 SystemDriver.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Metodo Change della classe Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483564"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Metodo Change della classe Win32 \_ SystemDriver

Il metodo **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**servizio \_ Win32 SystemDriver**](win32-systemdriver.md) . Il parametro [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento poiché i servizi dipendono tra loro. Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.

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

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.

Constraints: accetta lo stesso valore del parametro *Name* .

Esempio: "ATDISK"

</dd> <dt>

*Nome percorso* \[ in\]
</dt> <dd>

Percorso completo del file eseguibile che implementa il servizio.

Esempio: *\\ systemroot \\ System32 \\ drivers \\afd.sys*

</dd> <dt>

*ServiceType* \[ in\]
</dt> <dd>

Tipo di servizi forniti ai processi che li chiamano.

<dt>

1 (0x1)
</dt> <dd>

Driver del kernel

</dd> <dt>

2 (0x2)
</dt> <dd>

Driver del file System

</dd> <dt>

4 (0x4)
</dt> <dd>

Adattatore

</dd> <dt>

8 (0x8)
</dt> <dd>

Driver di riconoscimento

</dd> <dt>

16 (0x10)
</dt> <dd>

Processo personale

</dd> <dt>

32 (0x20)
</dt> <dd>

Condividi processo

</dd> <dt>

256 (0x100)
</dt> <dd>

Processo interattivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ in\]
</dt> <dd>

Gravità dell'errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal sistema.

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

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio avvio**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio avvio**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema**


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico**


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inizio richiesta**


</dt> <dd>

Servizio per avviare il gestore di controllo del servizio quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**


</dt> <dd>

Servizio che non può essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

Valore che, se impostato su **true**, il servizio può creare o comunicare con le finestre sul desktop.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o. \\ Nome utente. Quando viene eseguito, il processo del servizio viene registrato utilizzando uno di questi due formati. Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente. Se viene specificata una stringa vuota, il servizio viene connesso come account LocalSystem. Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ad esempio \\ filesystem \\ RDR o \\ driver \\ XNS, che il sistema di input e output (i/O) USA per caricare il driver di dispositivo. Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio, ad esempio DWDOM \\ admin.

È anche possibile usare il formato del nome dell'entità utente (UPN) per specificare il nome **iniziale**, ad esempio *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ in\]
</dt> <dd>

Password per il nome dell'account specificato dal parametro *StartName* . Specificare **null** se non si sta modificando la password. Specificare una stringa vuota se il servizio non dispone di password.

> [!Note]  
> Quando si modifica un servizio da un sistema locale a una rete o da una rete a un sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Nome del gruppo a cui è associato. I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo. Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* . I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo. Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:

**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ in\]
</dt> <dd>

Elenco di gruppi di ordini di caricamento che devono essere avviati prima dell'avvio del servizio. La matrice è con doppia terminazione **null**. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file WinSvc. h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*ServiceDependencies* \[ in\]
</dt> <dd>

Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. La matrice è con doppia terminazione **null**. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a zero (0) se il servizio è stato modificato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Servizi dipendenti in esecuzione** (3)
</dt> <dt>

**Controllo del servizio non valido** (4)
</dt> <dt>

Il **servizio non può accettare il controllo** (5)
</dt> <dt>

**Servizio non attivo** (6)
</dt> <dt>

**Timeout richiesta di servizio** (7)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Servizio già in esecuzione** (10)
</dt> <dt>

**Database del servizio bloccato** (11)
</dt> <dt>

**Dipendenza servizio eliminata** (12)
</dt> <dt>

**Errore di dipendenza del servizio** (13)
</dt> <dt>

**Servizio disabilitato** (14)
</dt> <dt>

**Accesso al servizio non riuscito** (15)
</dt> <dt>

**Servizio contrassegnato per l'eliminazione** (16)
</dt> <dt>

**Servizio senza thread** (17)
</dt> <dt>

**Stato dipendenza circolare** (18)
</dt> <dt>

**Stato nome duplicato** (19)
</dt> <dt>

**Stato nome non valido** (20)
</dt> <dt>

**Stato parametro non valido** (21)
</dt> <dt>

**Stato account del servizio non valido** (22)
</dt> <dt>

Il **servizio di stato esiste** (23)
</dt> <dt>

**Servizio già sospeso** (24)
</dt> <dt>

**Altro** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Per modificare un servizio da un servizio di rete al sistema locale, usare i valori seguenti per i parametri *StartName* e *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Per modificare un servizio da un servizio di sistema locale al servizio di rete, usare i valori seguenti per i parametri *StartName* e *StartPassword* :


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

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

