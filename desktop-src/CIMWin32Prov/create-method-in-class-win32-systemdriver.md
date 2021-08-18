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
ms.openlocfilehash: a85b18a04672f63c4f1fd8fe4fa386ffb4e3094e817b53a20af9887a84748a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080155"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Metodo Create della classe SystemDriver Win32 \_

Il **metodo Crea** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo servizio gestito dal driver di sistema. Il *parametro \_ LoadOrderGroup Win32* rappresenta un raggruppamento di servizi di sistema che definiscono le dipendenze di esecuzione. I servizi devono essere avviati nell'ordine specificato dal gruppo di ordini di carico, in quanto i servizi dipendono l'uno dall'altro. Per il corretto funzionamento di questi servizi dipendenti è necessaria la presenza dei servizi antecenti.

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*Nome* \[ Pollici\]
</dt> <dd>

Nome del servizio da installare nel **metodo Create.** La lunghezza massima della stringa è di 256 caratteri. Il database di Gestione controllo servizi mantiene la distinzione tra maiuscole e minuscole dei caratteri, ma i confronti tra i nomi dei servizi non esentengono sempre la distinzione tra maiuscole e minuscole. Le barre (/) e le doppie barre rovesciata ( \\ ) sono caratteri del nome di servizio non validi.

</dd> <dt>

*DisplayName* \[ Pollici\]
</dt> <dd>

Nome visualizzato del servizio. La lunghezza massima della stringa è di 256 caratteri. Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi. *Per i confronti displayName* non viene sempre fatto distinzione tra maiuscole e minuscole.

Vincoli: accetta lo stesso valore del *parametro Name.*

Esempio: "Atdisk".

</dd> <dt>

*PathName* \[ Pollici\]
</dt> <dd>

Percorso completo del file eseguibile che implementa il servizio.

Esempio: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys".

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

Gravità dell'errore se non **è possibile avviare** il metodo Create. Questo valore indica l'azione eseguita dal programma di avvio in caso di errore. Tutti gli errori vengono registrati dal sistema.

<dt>

0
</dt> <dd>

"Ignora"

L'utente non viene notificato.

</dd> <dt>

1
</dt> <dd>

"Normal"

L'utente viene notificato.

</dd> <dt>

2
</dt> <dd>

"Grave"

Il sistema viene riavviato con l'ultima configurazione valida nota.

</dd> <dt>

3
</dt> <dd>

"Critico"

Il sistema tenta di iniziare con una configurazione valida.

</dd> </dl> </dd> <dt>

*StartMode* \[ Pollici\]
</dt> <dd>

Modalità di avvio del Windows di base.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Avvio**


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

Servizio che deve essere avviato automaticamente da Gestione controllo servizi durante l'avvio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuale**


</dt> <dd>

Servizio che deve essere avviato da Gestione controllo servizi quando un processo chiama il [**metodo StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabili**


</dt> <dd>

Servizio che non può più essere avviato.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ Pollici\]
</dt> <dd>

Se **true,** il servizio può creare o comunicare con le finestre sul desktop.

</dd> <dt>

*StartName* \[ Pollici\]
</dt> <dd>

Nome dell'account con cui viene eseguito il servizio. A seconda del tipo di servizio, il nome dell'account può essere nel formato NomeDominioNomeUtente o Nome entità \\ utente (UPN) ( Username@DomainName ). Il processo del servizio viene registrato usando uno di questi due formati durante l'esecuzione. Se l'account appartiene al dominio predefinito, . \\ È possibile specificare il nome utente. Se viene specificato **NULL,** il servizio viene connesso come account LocalSystem. Per un kernel o driver a livello di sistema, *StartName* contiene il nome dell'oggetto driver (ovvero FileSystem Rdr o Driver Xns) che il sistema di input e \\ output \\ \\ (I/O) usa per caricare il driver di \\ dispositivo. Se **viene specificato NULL,** il driver viene eseguito con un nome di oggetto predefinito creato dal sistema di I/O in base al nome del servizio.

Esempio: Amministratore \\ DWDOM

</dd> <dt>

*StartPassword* \[ Pollici\]
</dt> <dd>

Password per il nome dell'account specificato dal *parametro StartName.* Specificare **NULL** se la password non viene cambiata. Specificare una stringa vuota se il servizio non dispone di password.

</dd> <dt>

*LoadOrderGroup* \[ Pollici\]
</dt> <dd>

Nome del gruppo associato al nuovo servizio. I gruppi degli ordini di carico sono contenuti nel Registro di sistema e determinano la sequenza in cui i servizi vengono caricati nel sistema operativo. Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non appartiene a un gruppo. Le dipendenze tra gruppi devono essere elencate nel *parametro LoadOrderGroupDependencies.* I servizi nell'elenco dei gruppi di ordinamento del carico vengono avviati per primi, seguiti dai servizi in gruppi non presenti nell'elenco di gruppi di ordinamento del carico, seguiti dai servizi che non appartengono a un gruppo. Il Registro di sistema include un elenco di gruppi di ordinamento del carico disponibili in:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*Dipendenze di LoadOrderGroupDependencies* \[ Pollici\]
</dt> <dd>

Matrice di gruppi di ordinamento del carico che devono essere avviati prima di questo servizio. Ogni elemento nella matrice è delimitato da **NULL** e l'elenco termina con due **valori NULL.** In Visual Basic o script è possibile passare un oggetto vbArray. Se il puntatore **è NULL** o punta a una stringa vuota, il servizio non ha dipendenze. I nomi dei gruppi devono essere preceduti dal carattere **SC \_ GROUP \_ IDENTIFIER** (definito nel file Winsvc.h) per distinguerlo da un nome di servizio, perché i servizi e i gruppi di servizi condividono lo stesso spazio dei nomi. La dipendenza da un gruppo significa che il servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

</dd> <dt>

*Dipendenze dei servizi* \[ Pollici\]
</dt> <dd>

Matrice che contiene i nomi dei servizi che devono essere avviati prima dell'avvio del servizio. Ogni elemento nella matrice è delimitato da **NULL** e l'elenco termina con due **valori NULL.** In Visual Basic o script è possibile passare un oggetto vbArray. Se il puntatore **è NULL** o se punta a una stringa vuota, il servizio non ha dipendenze. La dipendenza da un servizio significa che il servizio può essere eseguito solo se il servizio da cui dipende è in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il servizio è stato creato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

