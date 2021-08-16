---
description: Usare i metodi e le proprietà dell'oggetto SWbemObjectPath per costruire e convalidare il percorso di un oggetto. Questo oggetto può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Oggetto SWbemObjectPath (Wbemdisp.h)
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
ms.openlocfilehash: 2d7273b39c5cdccea7e46a077c925247846cd9ca255fc1dba20a95aeb159b773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313550"
---
# <a name="swbemobjectpath-object"></a>Oggetto SWbemObjectPath

Usare i metodi e le proprietà **dell'oggetto SWbemObjectPath** per costruire e convalidare il percorso di un oggetto. Questo oggetto può essere creato dalla chiamata **CreateObject di** VBScript.

## <a name="members"></a>Membri

**L'oggetto SWbemObjectPath** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemObjectPath** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**Classe SetAs**](swbemobjectpath-setasclass.md)         | Forza il percorso a una classe WMI.<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | Forza il percorso a un'istanza WMI singleton.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemObjectPath** ha queste proprietà.



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Authority**](swbemobjectpath-authority.md)<br/>             | Lettura/Scrittura<br/> | Stringa che definisce il componente Authority del percorso dell'oggetto.<br/>                                                                                                           |
| [**Classe**](swbemobjectpath-class.md)<br/>                     | Lettura/Scrittura<br/> | Nome della classe che fa parte del percorso dell'oggetto.<br/>                                                                                                                        |
| [**Displayname**](swbemobjectpath-displayname.md)<br/>         | Lettura/Scrittura<br/> | Stringa che contiene il percorso in un formato che può essere usato come nome visualizzato del moniker. Vedere [Creazione di un'applicazione WMI o di uno script.](creating-a-wmi-application-or-script.md)<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Sola lettura<br/>  | Valore booleano che indica se questo percorso rappresenta una classe. Questo è analogo alla proprietà [ \_ \_ Genus](wmi-system-properties.md) nell'API COM.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Sola lettura<br/>  | Valore booleano che indica se questo percorso rappresenta un'istanza singleton.<br/>                                                                                                |
| [**Chiavi**](swbemobjectpath-keys.md)<br/>                       | Sola lettura<br/>  | Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che contiene le associazioni del valore di chiave.<br/>                                                                          |
| [**Locale**](swbemobjectpath-locale.md)<br/>                   | Lettura/Scrittura<br/> | Stringa contenente le impostazioni locali per il percorso dell'oggetto.<br/>                                                                                                                     |
| [**Spazio dei nomi**](swbemobjectpath-namespace.md)<br/>             | Lettura/Scrittura<br/> | Nome dello spazio dei nomi che fa parte del percorso dell'oggetto. Corrisponde alla proprietà [ \_ \_ Namespace](wmi-system-properties.md) nell'API COM.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Sola lettura<br/>  | Nome dell'elemento padre dello spazio dei nomi che fa parte del percorso dell'oggetto.<br/>                                                                                                      |
| [**Percorso**](swbemobjectpath-path.md)<br/>                       | Lettura/Scrittura<br/> | Contiene il percorso assoluto. Corrisponde alla proprietà di sistema [ \_ \_ Path](wmi-system-properties.md) nell'API COM. Si tratta della proprietà predefinita di questo oggetto.<br/>    |
| [**Percorso relpath**](swbemobjectpath-relpath.md)<br/>                 | Lettura/Scrittura<br/> | Contiene il percorso relativo. Corrisponde alla proprietà di [ \_ \_ sistema Relpath](wmi-system-properties.md) nell'API COM.<br/>                                              |
| [**Sicurezza\_**](swbemobjectpath-security-.md)<br/>            | Sola lettura<br/>  | Consente di leggere o modificare le impostazioni di sicurezza.<br/>                                                                                                                             |
| [**Server**](swbemobjectpath-server.md)<br/>                   | Lettura/Scrittura<br/> | Nome del server. Corrisponde alla proprietà di sistema [ \_ \_ Server](wmi-system-properties.md) nell'API COM.<br/>                                                       |



 

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato come compilare percorsi di oggetti.


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



L'esempio di codice Perl seguente illustra come compilare percorsi di oggetti.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




