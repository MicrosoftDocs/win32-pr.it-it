---
description: GetOwner&\# 8194; Il metodo della classe WMI recupera il nome utente e il nome di dominio in cui è in esecuzione il processo.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Metodo GetOwner della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126483"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Metodo GetOwner della classe di \_ processo Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** Recupera il nome utente e il nome di dominio in cui è in esecuzione il processo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Utente* \[ di out\]
</dt> <dd>

Restituisce il nome utente del proprietario del processo.

</dd> <dt>

*Dominio* \[ out\]
</dt> <dd>

Restituisce il nome di dominio in cui è in esecuzione il processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Esempio

[Il monitoraggio elaborazione CPU PCT per nome con proprietario](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) L'esempio VBScript raccoglie la percentuale di utilizzo della CPU o del processore e cerca il proprietario del processo.

L' [elenco di tutti i server in cui viene eseguito l'accesso a un elenco di utenti](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) in PowerShell esegue query su WMI per il proprietario di tutti i processi explorer.exe.

Nell'esempio di codice VBScript seguente viene ottenuto il proprietario per ogni processo in esecuzione.


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

