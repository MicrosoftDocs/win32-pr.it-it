---
description: I metodi e le proprietà dell'oggetto SWbemLastError contengono e modificano gli oggetti Error.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Oggetto SWbemLastError (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309846"
---
# <a name="swbemlasterror-object"></a>Oggetto SWbemLastError

I metodi e le proprietà dell'oggetto **SWbemLastError** contengono e modificano gli oggetti Error. I metodi e le proprietà di questo oggetto sono esattamente identici a quelli dell'oggetto [**SWbemObject**](swbemobject.md) , ma vengono usati per contenere informazioni sugli errori anziché le informazioni sulla classe WMI. Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.

È possibile creare un oggetto errore **SWbemLastError** per esaminare le informazioni estese sugli errori associate a una chiamata al metodo precedente. Se le informazioni sull'errore non sono disponibili, un tentativo di creare un oggetto Error avrà esito negativo. Se la chiamata ha esito positivo e viene restituito un oggetto Error, viene reimpostato lo stato dell'oggetto. Ulteriori tentativi di recupero di un oggetto Error avranno esito negativo fino a quando non si verifica un nuovo errore. Se si effettua una chiamata asincrona che ha esito negativo, un oggetto **SWbemLastError** può essere restituito dall'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) nel parametro *objWbemErrorObject* .

## <a name="members"></a>Membri

L'oggetto **SWbemLastError** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemLastError** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **ASSOCIATORS\_**                                        | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **AssociatorsAsync\_**                                   | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| [**Clone\_**](swbemlasterror-clone-.md)                 | Crea una copia dell'oggetto corrente.<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | Verifica l'uguaglianza di due oggetti.<br/>                                                   |
| **Delete\_**                                             | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **DeleteAsync\_**                                        | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **ExecMethod\_**                                         | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **ExecMethodAsync\_**                                    | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | Recupera la rappresentazione testuale dell'oggetto scritto con la sintassi MOF.<br/>       |
| **Istanze\_**                                          | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **InstancesAsync\_**                                     | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **Mettere\_**                                                | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **PutAsync\_**                                           | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **Riferimenti\_**                                         | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **ReferencesAsync\_**                                    | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **SpawnDerivedClass\_**                                  | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **SpawnInstance\_**                                      | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **Sottoclassi\_**                                         | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **SubclassesAsync\_**                                    | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemLastError** dispone di queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Derivazione\_**<br/>                                   | Sola lettura<br/> | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |
| **Metodi\_** <br/>                                     | Sola lettura<br/> | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |
| [**Percorso\_**](swbemlasterror-path-.md)<br/>             | Sola lettura<br/> | Contiene un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.<br/>                    |
| [**Proprietà\_**](swbemlasterror-properties-.md)<br/> | Sola lettura<br/> | Rappresenta la raccolta di proprietà dell'oggetto **SWbemLastError** . Questa proprietà è un oggetto [**SWbemPropertySet**](swbempropertyset.md) .<br/> |
| **Qualificatori\_**<br/>                                   | Sola lettura<br/> | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |
| **Sicurezza\_**<br/>                                     | Sola lettura<br/> | Non usato. L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |



 

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene illustrato come controllare le informazioni sugli oggetti Error e Error.


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



Nell'esempio Perl seguente viene illustrato come controllare le informazioni sugli oggetti Error e Error.


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
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
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMLASTERROR IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




