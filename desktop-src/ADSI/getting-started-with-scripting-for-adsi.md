---
title: Attività iniziali con scripting per ADSI
description: La creazione di script è utile per gli amministratori di sistema che desiderano creare script batch per le attività usate di frequente.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Attività iniziali con Scripting per ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a83da0194fb03cdb31430f389dbfbf64327806b1b142be3b9c1c5813696548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839954"
---
# <a name="getting-started-with-scripting-for-adsi"></a>Attività iniziali con scripting per ADSI

La creazione di script è utile per gli amministratori di sistema che desiderano creare script batch per le attività usate di frequente.

Per avviare lo scripting con ADSI, è necessario disporre di un computer che esegue Windows o essere connesso a un dominio che contiene i dati per gli account computer nella directory.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Esempio di scripting semplice: ricerca di nomi e percorsi di account computer

Creare un nuovo file di testo usando un editor di testo. Nell'esempio di codice seguente viene illustrato come trovare i nomi e i percorsi degli account computer.


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



Salvare il file come First.vbs. Modificare la riga che inizia con "objCommand.CommandText" per modificare il percorso del dominio. Al prompt dei comandi digitare **cscript First.vbs** riga di comando o First.vbs per Windows script. I risultati devono essere restituiti nel prompt dei comandi.

Per altre informazioni sullo scripting per ADSI, vedere Scripting delle interfacce [del servizio Active Directory.](adsi-scripting-tutorial.md)

 

 




