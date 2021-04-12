---
description: Un oggetto SWbemObjectSet è una raccolta di oggetti SWbemObject. Per ulteriori informazioni, vedere Accesso a una raccolta. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Oggetto SWbemObjectSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233798"
---
# <a name="swbemobjectset-object"></a>Oggetto SWbemObjectSet

Un oggetto **SWbemObjectSet** è una raccolta di oggetti [**SWbemObject**](swbemobject.md) . Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md). Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.

È possibile ottenere un oggetto **SWbemObjectSet** chiamando uno dei metodi seguenti o i relativi equivalenti asincroni:

-   [**SWbemObject. Associator\_**](swbemobject-associators-.md)
-   [**SWbemObject. Instances\_**](swbemobject-instances-.md)
-   [**SWbemObject. References\_**](swbemobject-references-.md)
-   [**SWbemObject. sottoclassi\_**](swbemobject-subclasses-.md)
-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> L'oggetto **SWbemObjectSet** non supporta i metodi facoltativi di **aggiunta** e **rimozione** della raccolta.

 

> [!Note]  
> Poiché è possibile che la chiamata al sink non venga restituita allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

## <a name="members"></a>Membri

L'oggetto **SWbemObjectSet** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemObjectSet** dispone di questi metodi.



| Metodo                              | Descrizione                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Elemento**](swbemobjectset-item.md) | Recupera un oggetto [**SWbemObject**](swbemobject.md) dalla raccolta. Si tratta del metodo predefinito dell'oggetto.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemObjectSet** dispone di queste proprietà.



| Proprietà                                                  | Tipo di accesso          | Descrizione                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Conteggio**](swbemobjectset-count.md)<br/>          | Sola lettura<br/> | Numero di elementi nella raccolta.<br/>        |
| [**Sicurezza\_**](swbemobjectset-security-.md)<br/> | Sola lettura<br/> | Utilizzato per leggere o modificare le impostazioni di sicurezza.<br/> |



 

## <a name="remarks"></a>Commenti

Un **SWbemObjectSet** è una raccolta di zero o più oggetti [**SWbemObject**](swbemobject.md) . Ogni **SWbemObject** in un **SWbemObjectSet** può rappresentare uno dei due elementi seguenti:

-   Istanza di una risorsa gestita da WMI.
-   Istanza di una definizione di classe.

L'uso più comune di questa classe in WMI è come valore restituito per una chiamata a [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) o [**InstancesOf**](swbemservices-instancesof.md) , come descritto nell'esempio di codice seguente:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



Nella maggior parte dei casi, l'unica cosa che si può fare con un **SWbemObjectSet** è enumerare tutti gli oggetti contenuti nella raccolta stessa. Tuttavia, **SWbemObjectSet** include un numero di proprietà che può essere utile per gli script di amministrazione del sistema. Come suggerisce il nome, Count indica il numero di elementi nella raccolta. Questo script, ad esempio, recupera una raccolta di tutti i servizi installati in un computer e quindi restituisce il numero totale di servizi trovati:

Per ulteriori informazioni sull'utilizzo di questa classe, vedere [enumerazione di WMI](enumerating-wmi.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato il modo in cui vengono modificate le raccolte di **SWbemObjectSet** .


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



Nell'esempio di codice Perl seguente viene illustrato come vengono modificate le raccolte di **SWbemObjectSet** .


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




