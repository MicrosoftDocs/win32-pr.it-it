---
description: Modifica un servizio \_ SystemDriver Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Modificare il metodo della Win32_SystemDriver classe (Mbnapi.h)
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
ms.openlocfilehash: 96ff327e84d3a5b6c66011506c162810f0fcc91d0cafe4053266aa8928f6e5a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925111"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Modificare il metodo della classe SystemDriver Win32 \_

Il **metodo Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**servizio \_ SystemDriver Win32.**](win32-systemdriver.md) Il [**parametro \_ LoadOrderGroup Win32**](win32-loadordergroup.md) rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo di ordini di carico, in quanto i servizi dipendono l'uno dall'altro. Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi antecenti.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*DisplayName* \[ Pollici\]
</dt> <dd>

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. *Per i confronti displayName* non viene sempre fatto distinzione tra maiuscole e minuscole.

Vincoli: accetta lo stesso valore del *parametro Name.*

Esempio: "Atdisk"

</dd> <dt>

*PathName* \[ Pollici\]
</dt> <dd>

Percorso completo del file eseguibile che implementa il servizio.

Esempio: *\\ driver \\ SystemRoot System32 \\ \\afd.sys*

</dd> <dt>

*ServiceType* \[ Pollici\]
</dt> <dd>

Tipo di servizi forniti ai processi che li chiamano.

<dt>

1 (0x1)
</dt> <dd>

Kernel Driver

</dd> <dt>

2 (0x2)
</dt> <dd>

File System Driver

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

Processo personalizzato

</dd> <dt>

32 (0x20)
</dt> <dd>

Processo di condivisione

</dd> <dt>

256 (0x100)
</dt> <dd>

Processo interattivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ Pollici\]
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

Il sistema viene riavviato con l'ultima configurazione valida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (3)


</dt> <dd>

Il sistema tenta un riavvio con una configurazione valida.

</dd> </dl> </dd> <dt>

*StartMode* \[ Pollici\]
</dt> <dd>

Modalità di avvio del servizio Windows base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio**


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

Servizio che viene avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della richiesta**


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabili**


</dt> <dd>

Servizio che non può essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ Pollici\]
</dt> <dd>

Valore che, se **True,** il servizio può creare o comunicare con le finestre sul desktop.

</dd> <dt>

*StartName* \[ Pollici\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato \\ NomeDominioNomeUtente o . \\ Nome utente. Quando viene eseguito, il processo del servizio viene registrato usando uno di questi due formati. Se l'account appartiene al dominio predefinito, . \\ È possibile specificare il nome utente. Se viene specificata una stringa vuota, il servizio viene connesso come account LocalSystem. Per i driver a livello di kernel o di sistema, *StartName* contiene il nome dell'oggetto driver, ad esempio FileSystem Rdr o Driver Xns, che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo. Se si specifica **NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio, ad esempio DWDOM \\ Admin.

È anche possibile usare il formato nome dell'entità utente (UPN) per specificare **startName,** ad esempio *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ Pollici\]
</dt> <dd>

Password del nome dell'account specificato dal *parametro StartName.* Specificare **NULL** se la password non viene cambiata. Specificare una stringa vuota se il servizio non dispone di password.

> [!Note]  
> Quando si modifica un servizio da un sistema locale a una rete o da una rete a un sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **NULL.**

 

</dd> <dt>

*LoadOrderGroup* \[ Pollici\]
</dt> <dd>

Nome del gruppo a cui è associato. I gruppi degli ordini di carico sono contenuti nel Registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non appartiene a un gruppo. Le dipendenze tra gruppi devono essere elencate nel *parametro LoadOrderGroupDependencies.* I servizi nell'elenco dei gruppi di ordinamento del carico vengono avviati per primi, seguiti dai servizi in gruppi non presenti nell'elenco di gruppi di ordinamento del carico, seguiti dai servizi che non appartengono a un gruppo. Il Registro di sistema include un elenco di gruppi di ordinamento del carico disponibili in:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*Dipendenze di LoadOrderGroupDependencies* \[ Pollici\]
</dt> <dd>

Elenco di gruppi di ordinamento del carico che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **null** con terminazione. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file WinSvc.h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che il servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*Dipendenze dei servizi* \[ Pollici\]
</dt> <dd>

Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **null** con terminazione. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio significa che il servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore zero (0) se il servizio è stato modificato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Servizi dipendenti in esecuzione** (3)
</dt> <dt>

**Controllo del servizio non valido** (4)
</dt> <dt>

**Il servizio non può accettare il controllo** (5)
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

**Dipendenza del servizio eliminata** (12)
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

**Dipendenza circolare dello stato** (18)
</dt> <dt>

**Nome duplicato stato** (19)
</dt> <dt>

**Nome stato non valido** (20)
</dt> <dt>

**Parametro stato non valido** (21)
</dt> <dt>

**Stato Account del servizio non valido** (22)
</dt> <dt>

**Servizio di stato esistente** (23)
</dt> <dt>

**Servizio già in pausa** (24)
</dt> <dt>

**Altro** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Per modificare un servizio da un servizio di rete al sistema locale, usare i valori seguenti per i *parametri StartName* *e StartPassword:*


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Per modificare un servizio da un servizio di sistema locale a un servizio di rete, usare i valori seguenti per i *parametri StartName* *e StartPassword:*


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
| Intestazione<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

