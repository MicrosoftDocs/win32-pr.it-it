---
description: Il metodo della classe WMI Pause sospende un processo di stampa.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Metodo Pause della classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1448e993a88f2f5ce800de041779fb66f383c8973143b90200622758511ef337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752821"
---
# <a name="pause-method-of-the-win32_printjob-class"></a>Metodo Pause della classe PrintJob Win32 \_

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Pause** sospende un processo di stampa.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.

<dl> <dt>

**0**
</dt> <dd>

Operazione completata

</dd> <dt>

**5**
</dt> <dd>

Accesso negato

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio di codice VBScript [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) (Sospendi tutte le stampanti con code di stampa vuote) sospende tutte le stampanti che non hanno processi di stampa in sospeso.

L'esempio di codice VBScript seguente sospende tutti i processi di stampa in un server di stampa.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> <dt>

[**Processo di stampa \_ Win32**](win32-printjob.md)
</dt> </dl>

 

