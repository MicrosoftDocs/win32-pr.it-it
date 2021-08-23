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
ms.openlocfilehash: 2fe91ef581490ab15869fa45c299c9e172c01df9d689a4fcd1546cbbf84621ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760441"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Metodo GetOwner della classe Win32 \_ Process

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** recupera il nome utente e il nome di dominio con cui è in esecuzione il processo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Utente* \[ Cambio\]
</dt> <dd>

Restituisce il nome utente del proprietario del processo.

</dd> <dt>

*Dominio* \[ Cambio\]
</dt> <dd>

Restituisce il nome di dominio in cui è in esecuzione il processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento riuscito** (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegi insufficienti** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non** valido (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Esempio

[Monitor Process CPU Pct by Name with Owner (Monitor Process CPU Pct by Name with Owner)](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) L'esempio VBScript raccoglie la percentuale di utilizzo della CPU o del processore e cerca il proprietario del processo.

Get [all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.

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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Processo \_ Win32**](win32-process.md)
</dt> </dl>

 

