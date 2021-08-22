---
description: Pianifica l'esecuzione di Autochk nell'unità disco rappresentata dal disco logico Win32 al successivo riavvio, se la dirty bit \_ è impostata.
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
ms.openlocfilehash: 7e4920bdded79a7f63cbe7beaf28a70837ad7a47c2b28a1e37d83208b4f4e6f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588191"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Metodo ScheduleAutoChk della classe LogicalDisk Win32 \_

Il **metodo della classe ScheduleAutoChk** pianifica l'esecuzione di Autochk nell'unità disco rappresentata da [**\_ LogicalDisk Win32**](win32-logicaldisk.md) al riavvio successivo, se la dirty bit è impostata.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disco logico* \[ Pollici\]
</dt> <dd>

Specifica l'elenco di unità da pianificare per Autochk al riavvio successivo. La sintassi della stringa è costituita dalla lettera di unità seguita da due punti per il disco logico, ad esempio: "C:"

> [!Note]  
> Controllare sempre la validità delle lettere di unità nella matrice *LogicalDisk* quando i dati provengono da un'origine sconosciuta o da un'origine non attendibile.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e un altro valore se si verifica un altro errore. I valori sono elencati nell'elenco seguente. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Nessun errore** (0)
</dt> <dt>

**Errore - Unità remota** (1)
</dt> <dt>

**Errore - Unità rimovibile** (2)
</dt> <dt>

**Errore - Unità non directory radice** (3)
</dt> <dt>

**Errore - Unità sconosciuta** (4)
</dt> </dl>

## <a name="remarks"></a>Commenti

Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer. Questo metodo non è applicabile alle unità logiche mappate.

## <a name="examples"></a>Esempio

Gli esempi di VBScript e PowerShell seguenti Autochk.exe l'esecuzione nell'unità C al successivo riavvio del computer.


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Disco logico \_ Win32**](win32-logicaldisk.md)
</dt> </dl>

 

