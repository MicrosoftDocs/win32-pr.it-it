---
description: Fornisce una connessione a una stampante esistente sulla rete e la aggiunge all'elenco delle stampanti disponibili.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Metodo AddPrinterConnection della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877417"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a>Metodo AddPrinterConnection della \_ classe Printer Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** fornisce una connessione a una stampante esistente sulla rete e la aggiunge all'elenco delle stampanti disponibili.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome descrittivo per la stampante.

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

</dd> <dt>

**1930**
</dt> <dd>

Driver della stampante incompatibile

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) di PowerShell installa tutti i driver della stampante da un server di stampa specificato.

L'esempio [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell elenca le stampanti condivise in un computer remoto e consente di aggiungere una connessione alla stampante dal computer remoto al computer.

Nell'esempio di codice VBScript seguente viene aggiunta una stampante locale.


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
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

[Attività WMI: stampanti e stampa](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**\_Stampante Win32**](win32-printer.md)
</dt> </dl>

 

