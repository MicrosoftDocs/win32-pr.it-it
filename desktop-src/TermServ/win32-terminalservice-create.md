---
title: Metodo Create della classe Win32_Service (Servizi Desktop remoto)
description: Crea un nuovo servizio di sistema.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44d6c67e0d5bd6333f57c44cc44c25dc64e04a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477710"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a>Metodo Create della classe Win32_Service (Servizi Desktop remoto)

Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio di sistema.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
  [in] string  Name,
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

*Nome* \[ in\]
</dt> <dd>

Nome del servizio da installare nel metodo **create** . La lunghezza massima della stringa è 256 caratteri. Il database di gestione controllo servizi conserva la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra nomi di servizio non fanno distinzione tra maiuscole e minuscole. Barre (/) e barre rovesciate doppie ( \) sono caratteri del nome del servizio non validi.

</dd> <dt>

*DisplayName* \[ in\]
</dt> <dd>

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi. I confronti *DisplayName* sono sempre senza distinzione tra maiuscole e minuscole.

Constraints: accetta lo stesso valore del parametro *Name* .

Esempio: "ATDISK".

</dd> <dt>

*Nome percorso* \[ in\]
</dt> <dd>

Percorso completo del file eseguibile che implementa il servizio.

Esempio: " \\ systemroot \\ system32 \\ drivers \\afd.sys".

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

Gravità dell'errore se non è possibile avviare il metodo **create** . Il valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal sistema.

<dt>

0
</dt> <dd>

L'utente non viene notificato.

</dd> <dt>

1
</dt> <dd>

L'utente viene notificato.

</dd> <dt>

2
</dt> <dd>

Il sistema viene riavviato con l'ultima configurazione valida nota.

</dd> <dt>

3
</dt> <dd>

Il sistema tenta di iniziare con una configurazione corretta.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Modalità di avvio del servizio di base di Windows.

<dt>

Avvio
</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

Sistema
</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

Automatico
</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

Manuale
</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](win32-terminalservice-startservice.md) .

</dd> <dt>

Disabled
</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

Se **true**, il servizio può creare o comunicare con Windows sul desktop.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o nome dell'entità utente (UPN) Username@DomainName . Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione. Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente. Se viene specificato **null** , il servizio viene connesso come account LocalSystem. Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero \\ filesystem \\ RDR o \\ driver \\ XNS) utilizzato dal sistema di input e output (i/O) per caricare il driver di dispositivo. Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio. Esempio: amministratore di DWDOM \\ .

</dd> <dt>

*StartPassword* \[ in\]
</dt> <dd>

Password per il nome dell'account specificato dal parametro *StartName* . Specificare **null** se non si sta modificando la password. Specificare una stringa vuota se il servizio non dispone di password.

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Nome del gruppo associato al nuovo servizio. I gruppi dell'ordine di caricamento sono contenuti nel registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non appartiene a un gruppo. Le dipendenze tra i gruppi devono essere elencate nel parametro *LoadOrderGroupDependencies* . I servizi nell'elenco di gruppi per l'ordine di caricamento vengono avviati per primi, seguiti da servizi nei gruppi non inclusi nell'elenco del gruppo di ordini di carico, seguiti da servizi che non appartengono a un gruppo. Nel registro di sistema è presente un elenco di gruppi di ordini di carico disponibili in:

**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ in\]
</dt> <dd>

Matrice di gruppi di ordini di caricamento che devono iniziare prima del servizio. Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** . In Visual Basic o script è possibile passare un vbArray. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti **dall' \_ \_ identificatore del gruppo SC** (definito nel file winsvc. h) per distinguerlo dal nome del servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*ServiceDependencies* \[ in\]
</dt> <dd>

Matrice che contiene i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. Ogni elemento nella matrice è delimitato da **null** e l'elenco viene terminato da due valori **null** . In Visual Basic o script è possibile passare un vbArray. Se il puntatore è **null** o se punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio significa che questo servizio può essere eseguito solo se è in esecuzione il servizio da cui dipende.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata accettata.

</dd> <dt>

**1**
</dt> <dd>

La richiesta non è supportata.

</dd> <dt>

**2**
</dt> <dd>

L'utente non dispone dell'accesso necessario.

</dd> <dt>

**3**
</dt> <dd>

Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.

</dd> <dt>

**4**
</dt> <dd>

Il codice di controllo richiesto non è valido o non è accettabile per il servizio.

</dd> <dt>

**5**
</dt> <dd>

Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio (proprietà di **stato** della classe [**\_ BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) è uguale a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

Il servizio non è stato avviato.

</dd> <dt>

**7**
</dt> <dd>

Il servizio non ha risposto in tempo utile alla richiesta di avvio.

</dd> <dt>

**8**
</dt> <dd>

Errore sconosciuto durante l'avvio del servizio.

</dd> <dt>

**9**
</dt> <dd>

Impossibile trovare il percorso di directory del file eseguibile del servizio.

</dd> <dt>

**10**
</dt> <dd>

Il servizio è già in esecuzione.

</dd> <dt>

**11**
</dt> <dd>

Il database a cui aggiungere il nuovo servizio è bloccato.

</dd> <dt>

**12**
</dt> <dd>

Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.

</dd> <dt>

**13**
</dt> <dd>

Impossibile trovare un servizio dipendente necessario.

</dd> <dt>

**14**
</dt> <dd>

Il servizio è stato disabilitato dal sistema.

</dd> <dt>

**15**
</dt> <dd>

Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.

</dd> <dt>

**16**
</dt> <dd>

Questo servizio verrà rimosso dal sistema.

</dd> <dt>

**17**
</dt> <dd>

Il servizio non dispone di un thread di esecuzione.

</dd> <dt>

**18**
</dt> <dd>

Il servizio ha dipendenze circolari all'avvio.

</dd> <dt>

**19**
</dt> <dd>

Un servizio è in esecuzione con lo stesso nome.

</dd> <dt>

**20**
</dt> <dd>

Il nome del servizio contiene caratteri non validi.

</dd> <dt>

**21**
</dt> <dd>

Sono stati passati parametri non validi al servizio.

</dd> <dt>

**22**
</dt> <dd>

L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.

</dd> <dt>

**23**
</dt> <dd>

Il servizio esiste già nel database dei servizi disponibili dal sistema.

</dd> <dt>

**24**
</dt> <dd>

Il servizio è attualmente sospeso nel sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

I servizi vengono in genere installati in uno dei due modi seguenti: come parte dell'installazione del sistema operativo o mediante un programma di installazione fornito dallo sviluppatore del servizio. Tuttavia, alcuni servizi, in particolare quelli creati internamente, potrebbero non avere un programma di installazione. In questi casi, è possibile usare il metodo **create** per installare i servizi a livello di codice.

Nonostante il nome, il metodo create non crea effettivamente un servizio. viene semplicemente installato un servizio esistente. Per usare questo comando, è necessario copiare il file eseguibile del servizio in un computer e quindi usare **Crea** per installare il servizio.

Il metodo **create** è simile al metodo [**Change**](win32-terminalservice-change.md) . In entrambi i casi, le proprietà del servizio vengono passate come parametri al metodo. Come per i parametri usati con il metodo **Change** , l'ordine in cui vengono passati questi parametri è molto importante.

Il parametro *LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro. Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classi del sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[Attività WMI: Servizi](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

