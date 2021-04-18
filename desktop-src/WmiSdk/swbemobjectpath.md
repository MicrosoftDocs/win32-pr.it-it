---
description: Usare i metodi e le proprietà dell'oggetto SWbemObjectPath per creare e convalidare il percorso di un oggetto. Questo oggetto può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Oggetto SWbemObjectPath (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309805"
---
# <a name="swbemobjectpath-object"></a>Oggetto SWbemObjectPath

Usare i metodi e le proprietà dell'oggetto **SWbemObjectPath** per creare e convalidare il percorso di un oggetto. Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemObjectPath** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemObjectPath** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | Impone al percorso di indirizzare una classe WMI.<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | Impone al percorso di indirizzare un'istanza WMI singleton.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemObjectPath** dispone di queste proprietà.



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Authority**](swbemobjectpath-authority.md)<br/>             | Lettura/Scrittura<br/> | Stringa che definisce il componente Authority del percorso dell'oggetto.<br/>                                                                                                           |
| [**Classe**](swbemobjectpath-class.md)<br/>                     | Lettura/Scrittura<br/> | Nome della classe che fa parte del percorso dell'oggetto.<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | Lettura/Scrittura<br/> | Stringa che contiene il percorso in un form che può essere utilizzato come nome visualizzato del moniker. Vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Sola lettura<br/>  | Valore booleano che indica se questo percorso rappresenta una classe. Questo è analogo alla proprietà [ \_ \_ genre](wmi-system-properties.md) nell'API com.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Sola lettura<br/>  | Valore booleano che indica se questo percorso rappresenta un'istanza singleton.<br/>                                                                                                |
| [**Chiavi**](swbemobjectpath-keys.md)<br/>                       | Sola lettura<br/>  | Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che contiene le associazioni del valore della chiave.<br/>                                                                          |
| [**Locale**](swbemobjectpath-locale.md)<br/>                   | Lettura/Scrittura<br/> | Stringa contenente le impostazioni locali per il percorso dell'oggetto.<br/>                                                                                                                     |
| [**Spazio dei nomi**](swbemobjectpath-namespace.md)<br/>             | Lettura/Scrittura<br/> | Nome dello spazio dei nomi che fa parte del percorso dell'oggetto. Corrisponde alla proprietà [ \_ \_ namespace](wmi-system-properties.md) nell'API com.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Sola lettura<br/>  | Nome dell'elemento padre dello spazio dei nomi che fa parte del percorso dell'oggetto.<br/>                                                                                                      |
| [**Percorso**](swbemobjectpath-path.md)<br/>                       | Lettura/Scrittura<br/> | Contiene il percorso assoluto. Corrisponde alla proprietà di sistema [ \_ \_ path](wmi-system-properties.md) nell'API com. Si tratta della proprietà predefinita di questo oggetto.<br/>    |
| [**RelPath**](swbemobjectpath-relpath.md)<br/>                 | Lettura/Scrittura<br/> | Contiene il percorso relativo. Corrisponde alla proprietà di sistema [ \_ \_ RelPath](wmi-system-properties.md) nell'API com.<br/>                                              |
| [**Sicurezza\_**](swbemobjectpath-security-.md)<br/>            | Sola lettura<br/>  | Utilizzato per leggere o modificare le impostazioni di sicurezza.<br/>                                                                                                                             |
| [**Server**](swbemobjectpath-server.md)<br/>                   | Lettura/Scrittura<br/> | Nome del server. Corrisponde alla proprietà di sistema del [ \_ \_ server](wmi-system-properties.md) nell'API com.<br/>                                                       |



 

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato come compilare i percorsi degli oggetti.


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



Nell'esempio di codice Perl seguente viene illustrato come compilare i percorsi degli oggetti.


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                       |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




