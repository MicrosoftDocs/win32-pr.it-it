---
description: Win32Shutdown &\# 8194; Il metodo della classe WMI fornisce il set completo di opzioni di arresto supportate dai sistemi operativi Win32. Sono inclusi la disconnessione, l'arresto, il riavvio e la forzatura di una disconnessione, un arresto o un riavvio.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Metodo Win32Shutdown della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878214"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Metodo Win32Shutdown della \_ classe OperatingSystem Win32

Il metodo della   [classe WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** fornisce il set completo di opzioni di arresto supportate dai sistemi operativi Win32. Sono inclusi la disconnessione, l'arresto, il riavvio e la forzatura di una disconnessione, un arresto o un riavvio.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](../wmisdk/calling-a-method.md).

## <a name="syntax"></a>Sintassi


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Set di flag bitmap per arrestare il computer. Per forzare un comando, aggiungere il flag di forzatura (4) al valore del comando. L'utilizzo di Force in combinazione con l'arresto o il riavvio di un computer remoto arresta immediatamente tutti gli elementi, inclusi WMI, COM e così via, oppure riavvia il computer remoto. Ciò comporta un valore restituito indeterminato.

<dt>

0 (0x0)
</dt> <dd>

**Disconnetti** : disconnette l'utente dal computer. La disconnessione arresta tutti i processi associati al contesto di sicurezza del processo che ha chiamato la funzione Exit, registra l'utente corrente dal sistema e visualizza la finestra di dialogo Logon.

</dd> <dt>

4 (0x4)
</dt> <dd>

**Disconnessione forzata (0 + 4)** : disconnette immediatamente l'utente dal computer e non notifica alle applicazioni che la sessione di accesso sta per terminare. Ciò può comportare la perdita di dati.

</dd> <dt>

1 (0x1)
</dt> <dd>

**Arresta** : arresta il computer fino a un punto in cui è sicuro spegnere la potenza. Tutti i buffer di file vengono scaricati su disco e tutti i processi in esecuzione vengono arrestati. Il messaggio viene visualizzato dagli utenti, `It is now safe to turn off your computer.`

Durante l'arresto, il sistema invia un messaggio a ogni applicazione in esecuzione. Le applicazioni eseguono qualsiasi pulizia durante l'elaborazione del messaggio e restituiscono true per indicare che possono essere interrotte.

</dd> <dt>

5 (0x5)
</dt> <dd>

**Arresto forzato (1 + 4)** -arresta il computer fino a un punto in cui è sicuro spegnere la potenza. Tutti i buffer di file vengono scaricati su disco e tutti i processi in esecuzione vengono arrestati. Il messaggio viene visualizzato dagli utenti,` It is now safe to turn off your computer.`

Quando si usa l'approccio di arresto forzato, tutti i servizi, incluso WMI, vengono arrestati immediatamente. Per questo motivo, non sarà possibile ricevere un valore restituito se si esegue lo script in un computer remoto.

</dd> <dt>

2 (0x2)
</dt> <dd>

**Riavvia** : arresta e riavvia il computer.

</dd> <dt>

6 (0x6)
</dt> <dd>

**Riavvio forzato (2 + 4)** : arresta e riavvia il computer.

Quando si usa l'approccio per il riavvio forzato, tutti i servizi, incluso WMI, vengono arrestati immediatamente. Per questo motivo, non sarà possibile ricevere un valore restituito se si esegue lo script in un computer remoto.

</dd> <dt>

8 (0x8)
</dt> <dd>

**Spegnimento: arresta** il computer e disattiva la potenza (se supportata dal computer in questione).

</dd> <dt>

12 (0xC)
</dt> <dd>

Spegnimento **forzato (8 + 4)** -arresta il computer e disattiva la potenza (se supportata dal computer in questione).

Quando si usa l'approccio di spegnimento forzato, tutti i servizi, incluso WMI, vengono arrestati immediatamente. Per questo motivo, non sarà possibile ricevere un valore restituito se si esegue lo script in un computer remoto.

</dd> </dl> </dd> <dt>

*Riservato* \[ in\]
</dt> <dd>

Un metodo per estendere **Win32Shutdown**. Attualmente, il parametro *riservato* viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per i codici di errore, vedere [**costanti di errore WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](../debug/system-error-codes.md).

<dl> <dt>

**Operazione riuscita** (0)
</dt> <dt>

**Altro** (1-4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

Per una gestione più efficiente dei computer in un'organizzazione, gli amministratori hanno la possibilità di arrestare o riavviare un computer in modalità remota o di disconnettere un utente in remoto. La possibilità di eseguire queste attività consente agli amministratori di installare il software, riconfigurare le impostazioni del computer, rimuovere i computer dalla rete ed eseguire altre attività senza dover arrestare o riavviare manualmente ogni computer.

Ad esempio, per eseguire un aggiornamento della rete, potrebbe essere necessario arrestare tutti i computer in esecuzione in un particolare segmento di rete. Per forzare un aggiornamento Criteri di gruppo, è necessario disconnettere gli utenti dal computer. Se un virus del computer è presente in un punto qualsiasi dell'organizzazione, potrebbe essere necessario arrestare il maggior numero possibile di computer, prima che il virus abbia la possibilità di diffondersi. La possibilità di arrestare e riavviare i computer e di disconnettere gli utenti a livello di codice anziché manualmente può essere un notevole risparmio di tempo.

Il processo chiamante deve avere il privilegio di **\_ arresto del \_ nome** .

Il metodo [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) fornisce lo stesso set di opzioni di arresto supportate dal metodo **Win32Shutdown** in [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.

Il metodo Win32Shutdown non dispone di un parametro per il blocco di una workstation, lasciando l'utente connesso. Tuttavia, le workstation possono essere bloccate dalla riga di comando usando il comando seguente:

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>Esempio

L'esempio di [disconnessione, riavvio o arresto di più computer](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) in TechNet Gallery USA Win32Shutdown per disconnettersi, arrestare, riavviare o spegnere (a seconda della selezione) i computer elencati nell'array di server.

L'esempio [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell nella raccolta TechNet include un metodo che chiama Win32Shutdown in un computer remoto.

L'esempio di PowerShell seguente usa il metodo Win32Shutdown per arrestare il computer specificato.


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



L'esempio di codice PowerShell seguente usa il cmdlet EnableAllPrivileges di Get-WmiObject per ottenere il privilegi appropriato.


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



Il codice di esempio VB.NET seguente usa il metodo Shutdown per riavviare o disconnettersi da un sistema.


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**\_OperatingSystem Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[Attività WMI: gestione desktop](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
