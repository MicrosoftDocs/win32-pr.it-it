---
title: Introduzione con scripting per ADSI
description: Lo scripting è utile per gli amministratori di sistema che desiderano creare script batch per le attività utilizzate di frequente.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Introduzione con scripting per ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955095"
---
# <a name="getting-started-with-scripting-for-adsi"></a>Introduzione con scripting per ADSI

Lo scripting è utile per gli amministratori di sistema che desiderano creare script batch per le attività utilizzate di frequente.

Per avviare lo scripting con ADSI, è necessario disporre di un computer che esegua Windows o sia connesso a un dominio che contiene dati per gli account computer nella directory.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Esempio di scripting semplice: ricerca di nomi e percorsi di account computer

Creare un nuovo file di testo usando un editor di testo. Nell'esempio di codice riportato di seguito viene illustrato come individuare i nomi e i percorsi degli account computer.


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



Salvare il file come First.vbs. Modificare la riga che inizia con "objCommand. CommandText" per modificare il percorso del dominio. Al prompt dei comandi digitare **cscript First.vbs** per una riga di comando o First.vbs per Windows Scripting. I risultati devono essere restituiti nel prompt dei comandi.

Per ulteriori informazioni sullo scripting per ADSI, vedere [Active Directory le interfacce di servizio di scripting](adsi-scripting-tutorial.md).

 

 




