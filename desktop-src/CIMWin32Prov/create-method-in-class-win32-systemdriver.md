---
description: Crea un nuovo servizio gestito dal driver di sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127763"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Metodo Create della classe Win32 \_ SystemDriver

Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio gestito dal driver di sistema. Il parametro *Win32 \_ LoadOrderGroup* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo dell'ordine di caricamento, in quanto i servizi sono dipendenti tra loro. Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi precedenti.

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

Nome del servizio da installare nel metodo **create** . La lunghezza massima della stringa è 256 caratteri. Il database di gestione controllo servizi conserva la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra nomi di servizio non fanno distinzione tra maiuscole e minuscole. Le barre (/) e le barre rovesciate doppie ( \\ ) non sono caratteri validi per il nome del servizio.

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

Gravità dell'errore se non è possibile avviare il metodo **create** . Questo valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal sistema.

<dt>

0
</dt> <dd>

Ignorare

L'utente non viene notificato.

</dd> <dt>

1
</dt> <dd>

"Normal"

L'utente viene notificato.

</dd> <dt>

2
</dt> <dd>

Grave

Il sistema viene riavviato con l'ultima configurazione valida nota.

</dd> <dt>

3
</dt> <dd>

Critico

Il sistema tenta di iniziare con una configurazione corretta.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Modalità di avvio del servizio di base di Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**


</dt> <dd>

Driver di dispositivo avviato dal caricatore del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**


</dt> <dd>

Driver di dispositivo avviato dal processo di inizializzazione del sistema operativo. Questo valore è valido solo per i servizi del driver.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico**


</dt> <dd>

Servizio da avviare automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale**


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il metodo [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**


</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

Se **true**, il servizio può creare o comunicare con le finestre sul desktop.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato DomainName \\ username o nome dell'entità utente (UPN) Username@DomainName . Il processo del servizio viene registrato utilizzando una di queste due forme durante l'esecuzione. Se l'account appartiene al dominio predefinito,. \\ È possibile specificare il nome utente. Se viene specificato **null** , il servizio viene connesso come account LocalSystem. Per i driver del kernel o a livello di sistema, *StartName* contiene il nome dell'oggetto driver, ovvero \\ filesystem \\ RDR o \\ driver XNS, \\ usato dal sistema di input e output (i/O) per caricare il driver di dispositivo. Se viene specificato **null** , il driver viene eseguito con un nome di oggetto predefinito creato dal sistema i/O in base al nome del servizio.

Esempio: amministratore di DWDOM \\

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

Restituisce un valore pari a 0 (zero) se il servizio è stato creato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

