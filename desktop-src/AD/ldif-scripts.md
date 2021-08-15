---
title: Script LDIF
description: Ldap Data Interchange Format (LDIF) è uno standard IETF (Internet Engineering Task Force) che definisce come importare ed esportare i dati della directory tra server di directory che usano provider di servizi LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Script LDIF Active Directory
- Script LDIF Active Directory , informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad45c51fc16b3c19c3e59f4cfba2e006d4df900c20ce7ddc1b801478a22982c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187085"
---
# <a name="ldif-scripts"></a>Script LDIF

Ldap Data Interchange Format (LDIF) è uno standard IETF (Internet Engineering Task Force) che definisce come importare ed esportare i dati della directory tra server di directory che usano provider di servizi LDAP. Windows 2000 e Windows Server 2003 includono un'utilità della riga di comando, LDIFDE, che può essere usata per importare oggetti directory in Active Directory Domain Services file LDIF. LDIFDE consente di impostare un filtro su una stringa specifica per cercare ed elencare gli oggetti directory in Active Directory Domain Services come file LDIF che possono essere letti facilmente dagli amministratori dello schema.

Quando si importa un file Unicode, LDIFDE importa il file come Unicode se contiene l'identificatore Unicode all'inizio del file. Se si vuole importare un file come Unicode quando non contiene l'identificatore Unicode all'inizio del file, è possibile usare l'opzione -u per forzare l'importazione come Unicode.

La modalità predefinita per l'esportazione dei file è ANSI. Se sono presenti voci Unicode, verranno convertite in formato Base 64. Per esportare un file in formato Unicode, usare l'opzione -u.

Un file LDIF deve applicare le modifiche dello schema in caso di dipendenze tra gli attributi aggiunti. Ad esempio, gli attributi di collegamento in avanti devono essere aggiunti prima dell'attributo back link corrispondente. È inoltre necessario aggiornare la cache dello schema prima di aggiungere classi che dipendono da attributi o classi aggiunte in precedenza nello script LDIF. Per altre informazioni, vedere l'esempio di codice seguente.

Tenere presente che per i valori binari è necessario codificare i valori come base64. La codifica Base64 è definita in IETF RFC 2045, sezione 6.8.

Per altre informazioni sul formato dei file LDIF, vedere [LDIF (LDAP Data Interchange Format) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) nel sito Web Internet Engineering Task Force.

## <a name="ntds-specific-ldif-changetypes"></a>Tipi di modifica LDIF specifici di NTDS

È meglio usare i tipi di modifica ntdsSchema \* anziché chiamare ldifde -k. L'opzione -k di ldifde ignora un set più ampio di errori LDAP. L'elenco completo degli errori ignorati è il seguente:

-   L'oggetto è già membro del gruppo.
-   Violazione della classe di oggetti ,ovvero la classe di oggetti specificata non esiste, se l'oggetto importato non ha altri attributi.
-   L'oggetto esiste già (**LDAP \_ ALREADY \_ EXISTS**)
-   violazione di vincolo (**LDAP \_ CONSTRAINT \_ VIOLATION**)
-   L'attributo o il valore esiste già (**LDAP ATTRIBUTE OR VALUE \_ \_ \_ \_ EXISTS**)
-   nessun oggetto di questo tipo (**LDAP \_ NO SUCH \_ \_ OBJECT**)

I tipi di modifica seguenti sono progettati specificamente per le operazioni di aggiornamento dello schema.



| Changetype                      | Descrizione                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ntdsSchemaAdd**<br/>    | **ntdsSchemaAdd corrisponde** **all'aggiunta** in un file LDIF. L'unica differenza è che **ntdsSchemaAdd** fa sì  che ldifde ignorare un'operazione di aggiunta se l'oggetto esiste già nello schema. Ldap **\_ ALREADY EXISTS \_ viene** ignorato.<br/>                                   |
| **ntdsSchemaModify**<br/> | **ntdsSchemaModify** corrisponde alla **modifica** in un file LDIF. L'unica differenza è che **ntdsSchemaModify** fa sì  che ldifde ignorare un'operazione di modifica se l'oggetto non viene trovato nello schema. (LDAP **\_ NO SUCH \_ \_ OBJECT** viene ignorato).<br/>                        |
| **ntdsSchemaDelete**<br/> | **ntdsSchemaDelete corrisponde** **all'eliminazione** in un file LDIF. L'unica differenza è che **ntdsSchemaDelete** fa sì  che ldifde ignorare un'operazione di eliminazione se l'oggetto non viene trovato nello schema. (LDAP **\_ NO SUCH \_ \_ OBJECT** viene ignorato).<br/>                        |
| **ntdsSchemaModRdn**<br/> | **ntdsSchemaModRdn** corrisponde a **modrdn** in un file LDIF. L'unica differenza è che **ntdsSchemaModRdn** fa sì che ldifde ignorare un'operazione modify-relative-distinguished-name se l'oggetto non viene trovato nello schema. (LDAP **\_ NO SUCH \_ \_ OBJECT** viene ignorato).<br/> |



 

## <a name="example"></a>Esempio

L'esempio di codice seguente include:

-   Myschemaext.ldf è uno script LDIF che contiene nuovi attributi e classi. Tenere presente che questo file è una versione modificata del file generato da Lgetattcls.vbs. Tenere anche presente che l'attributo **My-Test-Attribute-DN-FL** è stato spostato prima di **My-Test-Attribute-DN-BL** perché il collegamento indietro (**My-Test-Attribute-DN-BL**) dipende dal collegamento in avanti (**My-Test-Attribute-DN-FL).** Inoltre, l'attributo operativo **schemaUpdateNow** viene impostato in due posizioni per attivare gli aggiornamenti della cache dello schema in modo che gli attributi e le classi dipendenti siano disponibili per l'aggiunta delle due classi nello script.
    > [!Note]  
    > Per informazioni [sull'origine](obtaining-a-link-id.md) dell'ID nelle istruzioni linkID:, vedere l'argomento Recupero di un ID collegamento.

     

-   Lgetattcls.vbs è un file VBScript che genera lo script LDIF usato come punto di partenza per Myschemaext.ldf. Tenere presente che il percorso dello schema corrente viene sostituito da CN=Schema,CN=Configuration,DC=myorg,DC=com. È possibile sostituire DC=myorg,DC=com per riflettere il nome distinto (DN) da pubblicare nello script LDIF, assicurarsi che LSETATTCLS.VBS rifletta la modifica nel relativo **sFromDN** in modo che il DN corretto viene sostituito quando viene applicato lo script LDIF. Tenere inoltre presente che lo script usa un prefisso per trovare le classi e gli attributi da definire e usare per tutte le classi e gli attributi. Per altre informazioni, vedere Naming [Attributes and Classes](naming-attributes-and-classes.md). Inoltre, lo script restituisce solo gli attributi necessari per gli oggetti **attributeSchema** e **classSchema** nel file LDIF.
-   Lsetattcls.vbs è un file VBScript che usa lo script Myschemaext.ldf per aggiungere i nuovi attributi e classi nello script. Verificare che il master dello schema sia in grado di scrivere in prima di eseguire lo script.

## <a name="myschemaextldf"></a>MYSCHEMAEXT. Ldf

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a>LGETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a>LSETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





