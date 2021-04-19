---
description: Il&di creazione \# 8194; Il metodo della classe WMI crea un nuovo processo.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304758"
---
# <a name="create-method-of-the-win32_process-class"></a>Metodo Create della classe di \_ processo Win32

Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo processo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Riga* \[ di comando in\]
</dt> <dd>

Riga di comando da eseguire. Il sistema aggiunge un carattere null alla riga di comando, tagliando la stringa se necessario, per indicare il file effettivamente utilizzato.

</dd> <dt>

*CurrentDirectory* \[ in\]
</dt> <dd>

Unità e directory correnti per il processo figlio. Per la stringa è necessario che la directory corrente venga risolta in un percorso noto. Un utente può specificare un percorso assoluto o un percorso relativo alla directory di lavoro corrente. Se questo parametro è **null**, il nuovo processo avrà lo stesso percorso del processo chiamante. Questa opzione viene fornita principalmente per le shell che devono avviare un'applicazione e specificare l'unità iniziale e la directory di lavoro dell'applicazione.

</dd> <dt>

*ProcessStartupInformation* \[ in\]
</dt> <dd>

Configurazione di avvio di un processo di Windows. Per ulteriori informazioni, vedere [**Win32 \_ ProcessStartup**](win32-processstartup.md).

</dd> <dt>

*ProcessID* \[ out\]
</dt> <dd>

Identificatore globale del processo che può essere usato per identificare un processo. Il valore è valido dal momento in cui il processo viene creato fino al momento in cui il processo viene terminato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il processo è stato creato correttamente e qualsiasi altro numero per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento** completato (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegio insufficiente** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non valido** (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

È possibile creare un'istanza della classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) per configurare il processo prima di chiamare questo metodo.

È necessario specificare un percorso completo nei casi in cui il programma da avviare non sia nel percorso di ricerca di Winmgmt.exe. Se il processo appena creato tenta di interagire con gli oggetti nel sistema di destinazione senza i privilegi di accesso appropriati, viene terminato senza notifica a questo metodo.

Per motivi di sicurezza, non è possibile usare il metodo **Win32 \_ Process. Create** per avviare un processo interattivo in modalità remota.

I processi creati con il metodo **Win32 \_ Process. Create** sono limitati dall'oggetto processo, a meno che non sia stato specificato il flag **Crea \_ fuga \_ dal \_ processo** . Per ulteriori informazioni, vedere [**Win32 \_ ProcessStartup**](win32-processstartup.md) e [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).

## <a name="examples"></a>Esempio

Nell'esempio VBScript riportato di seguito viene illustrato come richiamare un metodo CIM come se fosse un metodo di automazione di SWbemObject.


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



Nell'esempio Perl seguente viene illustrato come richiamare un metodo CIM come se fosse un metodo di automazione di SWbemObject.


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Nell'esempio di codice VBScript seguente viene creato un processo blocco note nel computer locale. [**Win32 \_ ProcessStartup**](win32-processstartup.md) viene usato per configurare le impostazioni del processo.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> <dt>

[Attività WMI: processi](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

