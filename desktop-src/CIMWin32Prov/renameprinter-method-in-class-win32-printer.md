---
description: Rinomina una stampante.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Metodo RenamePrinter della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225519"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a>Metodo RenamePrinter della \_ classe Printer Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenamePrinter** Rinomina una stampante.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewPrinterName* \[ in\]
</dt> <dd>

Nuovo nome della stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Operazione completata

</dd> <dt>

**5**
</dt> <dd>

Accesso negato

</dd> <dt>

**1801**
</dt> <dd>

Nome stampante non valido

</dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente vengono rinominate sia una stampante che il relativo nome di condivisione della stampante.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> <dt>

[**\_Stampante Win32**](win32-printer.md)
</dt> </dl>

 

