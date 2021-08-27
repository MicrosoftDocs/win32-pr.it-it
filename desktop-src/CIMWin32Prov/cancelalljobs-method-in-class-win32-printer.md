---
description: Rimuove tutti i processi, incluso quello attualmente in fase di stampa dalla coda.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Metodo CancelAllJobs della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06aae96cec4e38c7ff9c213cd19dc35e9843a077c262aafcaf0aed43160505a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085841"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a>Metodo CancelAllJobs della classe Printer Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CancelAllJobs** rimuove tutti i processi, incluso quello attualmente in fase di stampa dalla coda.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

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

[L'attività Notifica](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) agli utenti quando una coda di stampa viene eliminata usa Msg.exe per inviare un avviso di rete a tutti gli utenti che avevano documenti in una coda di stampa che sta per essere eliminati. Dopo l'invio degli avvisi, lo script elimina la coda di stampa.

[L'esempio di codice](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript Delete all print jobs (Elimina tutti i processi di stampa) elimina tutti i processi di stampa nel computer locale.

Nell'esempio vbscript seguente vengono eliminati tutti i processi di stampa per una stampante denominata HP QuietSample.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
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

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[**Stampante \_ Win32**](win32-printer.md)
</dt> </dl>

 

