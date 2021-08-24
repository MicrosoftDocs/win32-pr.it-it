---
description: Crea un nuovo driver della stampante.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Metodo AddPrinterDriver della Win32_PrinterDriver classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14681c381f8c8b9abbc5b28ec763b959854e2303b9a0b87af762238f4e5a8d27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752801"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Metodo AddPrinterDriver della classe PrinterDriver Win32 \_

Il **metodo della classe AddPrinterDriver** crea un nuovo driver della stampante.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DriverInfo* \[ Pollici\]
</dt> <dd>

Istanza della classe [**\_ PrinterDriver Win32**](win32-printerdriver.md) che rappresenta il driver della stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per valori diversi da quelli elencati nell'elenco seguente, vedere [**Costanti di errore WMI.**](/windows/desktop/WmiSdk/wmi-error-constants)

<dl> <dt>

**0**
</dt> <dd>

Operazione completata.

</dd> <dt>

**5**
</dt> <dd>

Accesso negato.

</dd> <dt>

**87**
</dt> <dd>

Parametro non corretto. Può verificarsi quando l'oggetto non è compilato correttamente o quando non è possibile trovare il driver nel sistema. In alternativa, l'attributo name può essere diverso dal modello specificato nel file inf. Oppure potrebbe essere presente una barra rovesciata mancante (" \\ ") in un attributo PathFile.

</dd> <dt>

**1797**
</dt> <dd>

Il driver della stampante è sconosciuto.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Quando si usa **il metodo AddPrinterDriver** è necessario usare **SeLoadDriverPrivilege** per caricare o scaricare un driver di dispositivo.

 

## <a name="examples"></a>Esempio

L'esempio di codice Install[a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript installa una stampante ipotetica usando un driver di stampa non trovato in Drivers.cab.

Nell'esempio VBScript seguente viene installato il driver della stampante per una stampante Apple® 8500.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
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

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

