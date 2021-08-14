---
description: I metodi e le proprietà dell'oggetto SWbemLastError contengono e modificano gli oggetti errore.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Oggetto SWbemLastError (Wbemdisp.h)
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
ms.openlocfilehash: a73312c38857b57f3ffeec8fcaf8a9ea5847001393d0a03d4916da76ffcb8c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314460"
---
# <a name="swbemlasterror-object"></a>Oggetto SWbemLastError

I metodi e le proprietà **dell'oggetto SWbemLastError** contengono e modificano gli oggetti errore. I metodi e le proprietà di questo oggetto sono esattamente uguali a quelli dell'oggetto [**SWbemObject,**](swbemobject.md) ma vengono usati per contenere informazioni sugli errori anziché informazioni sulla classe WMI. Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.

È possibile creare un **oggetto errore SWbemLastError** per esaminare le informazioni sull'errore esteso associate a una chiamata al metodo precedente. Se le informazioni sull'errore non sono disponibili, un tentativo di creare un oggetto errore avrà esito negativo. Se la chiamata ha esito positivo e viene restituito un oggetto errore, lo stato dell'oggetto viene reimpostato. Altri tentativi di recuperare un oggetto errore avranno esito negativo fino a quando non si verifica un nuovo errore. Se si effettua una chiamata asincrona che ha esito negativo, un **oggetto SWbemLastError** può essere restituito dall'evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) nel *parametro objWbemErrorObject.*

## <a name="members"></a>Membri

**L'oggetto SWbemLastError** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemLastError** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **Associators\_**                                        | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **AssociatorsAsync\_**                                   | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| [**Clone\_**](swbemlasterror-clone-.md)                 | Crea una copia dell'oggetto corrente.<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | Verifica l'uguaglianza di due oggetti.<br/>                                                   |
| **Elimina\_**                                             | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **DeleteAsync\_**                                        | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **ExecMethod\_**                                         | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **ExecMethodAsync\_**                                    | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | Recupera la rappresentazione testuale dell'oggetto scritto con la sintassi MOF.<br/>       |
| **Istanze\_**                                          | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **IstanzeAsync\_**                                     | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **Mettere\_**                                                | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **PutAsync\_**                                           | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **Riferimenti\_**                                         | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **ReferencesAsync\_**                                    | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **SpawnDerivedClass\_**                                  | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **SpawnInstance\_**                                      | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **Sottoclassi\_**                                         | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |
| **SottoclassiAsync\_**                                    | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemLastError** ha queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Derivazione\_**<br/>                                   | Sola lettura<br/> | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |
| **Metodi\_** <br/>                                     | Sola lettura<br/> | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |
| [**Percorso\_**](swbemlasterror-path-.md)<br/>             | Sola lettura<br/> | Contiene un [**oggetto SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.<br/>                    |
| [**Proprietà\_**](swbemlasterror-properties-.md)<br/> | Sola lettura<br/> | Rappresenta la raccolta di proprietà **dell'oggetto SWbemLastError.** Questa proprietà è un [**oggetto SWbemPropertySet.**](swbempropertyset.md)<br/> |
| **Qualificatori\_**<br/>                                   | Sola lettura<br/> | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |
| **Sicurezza\_**<br/>                                     | Sola lettura<br/> | Non usato. [**L'oggetto SWbemObject**](swbemobject.md) fornisce lo stesso metodo.<br/>                                                                  |



 

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene illustrato come esaminare le informazioni sugli oggetti error e error.


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



L'esempio Perl seguente illustra come esaminare le informazioni sugli oggetti error e error.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




