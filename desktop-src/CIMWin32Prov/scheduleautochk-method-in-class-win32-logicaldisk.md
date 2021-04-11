---
description: Pianifica Autochk da eseguire sull'unità disco rappresentata dal \_ disco logico Win32 al riavvio successivo se è impostato il bit modificato.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Metodo ScheduleAutoChk della classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966019"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Metodo ScheduleAutoChk della \_ classe disco logico Win32

Il metodo della classe **ScheduleAutoChk** pianifica l'esecuzione di Autochk sull'unità disco rappresentata dal [**\_ disco logico Win32**](win32-logicaldisk.md) al riavvio successivo se è impostato il bit dirty.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disco logico* \[ in\]
</dt> <dd>

Specifica l'elenco di unità da pianificare per Autochk al riavvio successivo. La sintassi della stringa è costituita dalla lettera di unità seguita da due punti per il disco logico, ad esempio: "C:"

> [!Note]  
> Controllare sempre la validità delle lettere di unità nella matrice *disco logico* quando i dati provengono da un'origine sconosciuta o da un'origine non attendibile.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se ha esito positivo e un altro valore se si verifica un altro errore. I valori sono elencati nell'elenco seguente. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Nessun errore** (0)
</dt> <dt>

**Errore-unità remota** (1)
</dt> <dt>

**Errore-unità rimovibile** (2)
</dt> <dt>

**Errore-unità non directory radice** (3)
</dt> <dt>

**Errore-unità sconosciuta** (4)
</dt> </dl>

## <a name="remarks"></a>Commenti

Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer. Questo metodo non è applicabile alle unità logiche mappate.

## <a name="examples"></a>Esempio

Gli esempi VBScript e PowerShell seguenti pianificano Autochk.exe per l'esecuzione sull'unità C alla successiva riavvio del computer.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
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

[**\_Disco logico Win32**](win32-logicaldisk.md)
</dt> </dl>

 

