---
description: Un oggetto SWbemPrivilegeSet è una raccolta di oggetti SWbemPrivilege in un oggetto SWbemSecurity che richiede privilegi specifici per un oggetto Strumentazione gestione Windows (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Oggetto SWbemPrivilegeSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344721"
---
# <a name="swbemprivilegeset-object"></a>Oggetto SWbemPrivilegeSet

Un oggetto **SWbemPrivilegeSet** è una raccolta di oggetti [**SWbemPrivilege**](swbemprivilege.md) in un oggetto [**SWbemSecurity**](swbemsecurity.md) che richiede privilegi specifici per un oggetto Strumentazione gestione Windows (WMI). Vedere l'elenco dei privilegi nelle [**costanti Privilege**](privilege-constants.md). Gli elementi vengono aggiunti alla raccolta usando i metodi [**Add**](swbemprivilegeset-add.md) e [**AddAsString**](swbemprivilegeset-addasstring.md) . Gli elementi vengono recuperati dalla raccolta usando il metodo [**Item**](swbemprivilegeset-item.md) e rimossi usando il metodo [**Remove**](swbemprivilegeset-remove.md) . Questo oggetto non può essere creato dalla chiamata al metodo [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript. Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).

Un oggetto **SWbemPrivilegeSet** è un set di richieste di override dei privilegi per un oggetto specifico. Quando viene eseguita una chiamata API utilizzando questo oggetto, vengono tentate le richieste di override dei privilegi. L'oggetto **SWbemPrivilegeSet** non definisce i privilegi disponibili per l'utente o il processo corrente. In altre parole, ottenendo i privilegi per qualsiasi oggetto WMI non vengono identificate le impostazioni dei privilegi effettuate sulla connessione a WMI oppure i privilegi attivi quando un oggetto viene recapitato a un sink.

## <a name="members"></a>Membri

L'oggetto **SWbemPrivilegeSet** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemPrivilegeSet** dispone di questi metodi.



| Metodo                                               | Descrizione                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](swbemprivilegeset-add.md)                 | Aggiunge un oggetto [**SWbemPrivilege**](swbemprivilege.md) alla raccolta **SWbemPrivilegeSet** usando una costante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .<br/> |
| [**AddAsString**](swbemprivilegeset-addasstring.md) | Aggiunge un oggetto [**SWbemPrivilege**](swbemprivilege.md) alla raccolta **SWbemPrivilegeSet** utilizzando una stringa di privilegio.<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Elimina tutti i privilegi dalla raccolta.<br/>                                                                                                              |
| [**Elemento**](swbemprivilegeset-item.md)               | Recupera un oggetto [**SWbemPrivilege**](swbemprivilege.md) dalla raccolta. Questo è il metodo predefinito di questo oggetto.<br/>                                 |
| [**Rimuovi**](swbemprivilegeset-remove.md)           | Rimuove un oggetto [**SWbemPrivilege**](swbemprivilege.md) dalla raccolta.<br/>                                                                              |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemPrivilegeSet** dispone di queste proprietà.



| Proprietà                                            | Tipo di accesso          | Descrizione                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Conteggio**](swbemprivilegeset-count.md)<br/> | Sola lettura<br/> | Numero di elementi nella raccolta.<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene ottenuto un oggetto SWbemPrivileges e vengono aggiunti tutti i privilegi disponibili alla raccolta in base al valore del privilegio, come definito in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



Nell'esempio di codice VBScript riportato di seguito viene illustrato come aggiungere privilegi utilizzando l'oggetto **SWbemPrivilegeSet** .


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



Nell'esempio di codice Perl seguente viene illustrato come aggiungere privilegi utilizzando l'oggetto **SWbemPrivilegeSet** .


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | \_SWBEMPRIVILEGESET CLSID<br/>                                                     |
| IID<br/>                      | \_ISWBEMPRIVILEGESET IID<br/>                                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> <dt>

[**Costanti Privilege**](privilege-constants.md)
</dt> </dl>

 

