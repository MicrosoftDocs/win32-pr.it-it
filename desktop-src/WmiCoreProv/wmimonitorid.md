---
description: Rappresenta le informazioni di identificazione relative a un monitor video, ad esempio il nome del produttore, l'anno di produzione o il numero di serie.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Classe WmiMonitorID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 552e66a4e3a0c6f120bcc95123e3a2674fc579457de16c9ef8cd1e80161f175e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051149"
---
# <a name="wmimonitorid-class"></a>Classe WmiMonitorID

La classe WMI **WmiMonitorID** rappresenta le informazioni di identificazione relative a un monitor video, ad esempio il nome del produttore, l'anno di produzione o il numero di serie. I dati in questa classe corrispondono ai dati nel blocco Vendor/Product Identification della definizione di input video dello standard VESA (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID).

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a>Members

La **classe WmiMonitorID** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WmiMonitorID** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del produttore.

</dd> <dt>

**ManufacturerNameLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lunghezza del nome del produttore che si trova nella **proprietà ManufacturerName.**

</dd> <dt>

**ProductCodeID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID del codice prodotto assegnato dal fornitore.

</dd> <dt>

**SerialNumberID**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di serie.

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo del monitoraggio. La dimensione del nome è la lunghezza specificata dalla proprietà UserFriendlyNameLength.

</dd> <dt>

UserFriendlyNameLength
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di caratteri nel nome che si trova nella proprietà UserFriendlyName.

</dd> <dt>

**WeekOfManufacture**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Settimana di produzione per numero di settimana. L'intervallo è compreso tra 1 e 53. Zero (0) non è definito.

</dd> <dt>

**YearOfManufacture**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Anno di produzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per informazioni su come convertire le matrici in cui sono archiviati gli ID dei numeri di serie, vedere l'articolo del blog Reporting [Monitor information with Gestione configurazione](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) (Monitoraggio report con Gestione configurazione di serie).

## <a name="examples"></a>Esempio

L'esempio di PowerShell seguente recupera il numero di serie di più monitor.


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



Il codice VBScript seguente recupera anche le informazioni sull'ID di monitoraggio da un sistema.


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

