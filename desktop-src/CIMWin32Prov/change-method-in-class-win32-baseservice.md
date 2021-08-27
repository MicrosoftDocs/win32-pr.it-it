---
description: Modifica un oggetto servizio derivato da Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Modificare il metodo della Win32_BaseService classe (Mbnapi.h)
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
ms.openlocfilehash: 306f771df0e44cb11ec61631b2d6b51f11ccefac9a719776d3a483d5cc861133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085831"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Modificare il metodo della classe BaseService Win32 \_

Il **metodo Change** WMI [class](/windows/desktop/WmiSdk/retrieving-a-class) modifica un oggetto servizio derivato da [**Win32 \_ BaseService.**](win32-baseservice.md) Il [**parametro \_ LoadOrderGroup Win32**](win32-loadordergroup.md) rappresenta un gruppo di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo di ordini di carico, perché i servizi dipendono l'uno dall'altro. Per il corretto funzionamento di questi servizi dipendenti sono necessari servizi antecenti.

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

Nome visualizzato per un servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto in Gestione controllo servizi. *Per i confronti displayName* non viene sempre fatto distinzione tra maiuscole e minuscole.

Vincoli: accetta lo stesso valore del *parametro Name.*

Esempio: "Atdisk".

</dd> <dt>

*PathName* \[ Pollici\]
</dt> <dd>

Percorso completo del file eseguibile che implementa un servizio.

Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ Pollici\]
</dt> <dd>

Tipo di servizi forniti ai processi che li chiamano.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver kernel** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver del file system** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver di riconoscimento** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Processo personale** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo di condivisione** (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Processo interattivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ Pollici\]
</dt> <dd>

Gravità di un errore se il servizio non viene avviato durante l'avvio. Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Il sistema registra tutti gli errori.

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

Modalità di avvio del Windows di base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Avvio ("Avvio")**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Avvio del sistema** ("Sistema")


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Avvio automatico** ("Automatico")


</dt> <dd>

Servizio che viene avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Avvio della domanda** ("manuale")


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-baseservice.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")


</dt> <dd>

Servizio che non può essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ Pollici\]
</dt> <dd>

Se **True,** il servizio può creare o comunicare con una finestra sul desktop.

</dd> <dt>

*StartName* \[ Pollici\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio, che dipende dal tipo di servizio. Il nome dell'account può essere nel formato \\ NomeDominioNomeUtente o . \\ Nome utente. Quando viene eseguito, il processo del servizio viene registrato usando uno dei due formati precedenti. Se l'account appartiene al dominio predefinito, . \\ È possibile specificare il nome utente. Se viene specificata una stringa vuota, il servizio viene connesso come account LocalSystem. Per i driver a livello di kernel o di sistema, *StartName* contiene il nome dell'oggetto driver, ad esempio FileSystem Rdr o Driver Xns, che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo. Se si specifica **NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio, ad esempio DWDOM \\ Admin.

È anche possibile usare il formato nome dell'entità utente (UPN) per specificare **startName,** ad esempio *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ Pollici\]
</dt> <dd>

Password per il nome dell'account specificato dal parametro *StartName.* Specificare **NULL** quando non si modifica la password. Specificare una stringa vuota se il servizio non dispone di una password.

> [!Note]  
> Quando si modifica un servizio da sistema locale a rete o da rete a sistema locale, *StartPassword* deve essere una stringa vuota ("") e non **NULL.**

 

</dd> <dt>

*LoadOrderGroup* \[ Pollici\]
</dt> <dd>

Nome del gruppo a cui è associato. I gruppi degli ordini di carico sono contenuti nel Registro di sistema e determinano la sequenza di caricamento dei servizi in un sistema operativo. Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non appartiene a un gruppo. Le dipendenze tra gruppi devono essere elencate nel *parametro LoadOrderGroupDependencies.* I servizi nell'elenco dei gruppi di ordinamento del carico vengono avviati per primi, seguiti dai servizi in gruppi non presenti nell'elenco di gruppi di ordinamento del carico, seguiti dai servizi che non appartengono a un gruppo. Il Registro di sistema include un elenco di gruppi di ordinamento del carico disponibili in **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.

</dd> <dt>

*Dipendenze di LoadOrderGroupDependencies* \[ Pollici\]
</dt> <dd>

Elenco di gruppi di ordinamento del carico che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **null** con terminazione. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file Winsvc.h) per distinguerli dai nomi dei servizi, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che il servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*Dipendenze dei servizi* \[ Pollici\]
</dt> <dd>

Elenco contenente i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. La matrice è doppiamente **null** con terminazione. Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio significa che il servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.

<dl> <dt>

**Success**
</dt> <dd>

0

La richiesta viene accettata.

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

Impossibile inviare il codice di controllo richiesto al servizio perché la proprietà [**State**](win32-baseservice.md) nell'oggetto [**Win32 \_ BaseService**](win32-baseservice.md) è uguale a 0, 1 o 2.

</dd> <dt>

**Servizio non attivo**
</dt> <dd>

6

Il servizio non è stato avviato.

</dd> <dt>

**Timeout della richiesta di servizio**
</dt> <dd>

7

Il servizio non risponde rapidamente alla richiesta di avvio.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

8

Processo interattivo.

</dd> <dt>

**Percorso non trovato**
</dt> <dd>

9

Impossibile trovare il percorso della directory del file eseguibile del servizio.

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

**Dipendenza del servizio eliminata**
</dt> <dd>

12

Una dipendenza su cui si basa questo servizio viene rimossa dal sistema.

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

Questo servizio viene rimosso dal sistema.

</dd> <dt>

**Nessun thread del servizio**
</dt> <dd>

17

Nessun thread di esecuzione per il servizio.

</dd> <dt>

**Dipendenza circolare dello stato**
</dt> <dd>

18

All'avvio del servizio sono state rilevate dipendenze circolari.

</dd> <dt>

**Nome duplicato dello stato**
</dt> <dd>

19

È presente un servizio in esecuzione con lo stesso nome.

</dd> <dt>

**Stato Nome non valido**
</dt> <dd>

20

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**Parametro stato non valido**
</dt> <dd>

21

Al servizio sono stati passati parametri non validi.

</dd> <dt>

**Stato Account del servizio non valido**
</dt> <dd>

22

L'account per l'esecuzione del servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.

</dd> <dt>

**Il servizio di stato esiste**
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

Per modificare un servizio da una rete a un sistema locale, usare i valori seguenti per i *parametri StartName* *e StartPassword:*


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Per modificare un servizio da un sistema locale a una rete, usare i valori seguenti per i *parametri StartName* *e StartPassword:*


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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

