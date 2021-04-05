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
# <a name="getting-started-with-scripting-for-adsi"></a><span data-ttu-id="58e4d-104">Introduzione con scripting per ADSI</span><span class="sxs-lookup"><span data-stu-id="58e4d-104">Getting Started with Scripting for ADSI</span></span>

<span data-ttu-id="58e4d-105">Lo scripting è utile per gli amministratori di sistema che desiderano creare script batch per le attività utilizzate di frequente.</span><span class="sxs-lookup"><span data-stu-id="58e4d-105">Scripting is useful for system administrators who want to create batch scripts for frequently used tasks.</span></span>

<span data-ttu-id="58e4d-106">Per avviare lo scripting con ADSI, è necessario disporre di un computer che esegua Windows o sia connesso a un dominio che contiene dati per gli account computer nella directory.</span><span class="sxs-lookup"><span data-stu-id="58e4d-106">To start scripting with ADSI, you must have a computer that runs Windows or be logged on to a domain that contains data for computer accounts in the directory.</span></span>

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a><span data-ttu-id="58e4d-107">Esempio di scripting semplice: ricerca di nomi e percorsi di account computer</span><span class="sxs-lookup"><span data-stu-id="58e4d-107">A Simple Scripting Sample: Finding Names and Locations of Computer Accounts</span></span>

<span data-ttu-id="58e4d-108">Creare un nuovo file di testo usando un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="58e4d-108">Create a new text file using a text editor.</span></span> <span data-ttu-id="58e4d-109">Nell'esempio di codice riportato di seguito viene illustrato come individuare i nomi e i percorsi degli account computer.</span><span class="sxs-lookup"><span data-stu-id="58e4d-109">The following code example shows how to find names and locations of computer accounts.</span></span>


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



<span data-ttu-id="58e4d-110">Salvare il file come First.vbs.</span><span class="sxs-lookup"><span data-stu-id="58e4d-110">Save the file as First.vbs.</span></span> <span data-ttu-id="58e4d-111">Modificare la riga che inizia con "objCommand. CommandText" per modificare il percorso del dominio.</span><span class="sxs-lookup"><span data-stu-id="58e4d-111">Modify the line that begins with "objCommand.CommandText" to change the path to your domain.</span></span> <span data-ttu-id="58e4d-112">Al prompt dei comandi digitare **cscript First.vbs** per una riga di comando o First.vbs per Windows Scripting.</span><span class="sxs-lookup"><span data-stu-id="58e4d-112">At the command prompt, type **cscript First.vbs** for a command line or First.vbs for Windows scripting.</span></span> <span data-ttu-id="58e4d-113">I risultati devono essere restituiti nel prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58e4d-113">The results should be returned in the command prompt.</span></span>

<span data-ttu-id="58e4d-114">Per ulteriori informazioni sullo scripting per ADSI, vedere [Active Directory le interfacce di servizio di scripting](adsi-scripting-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="58e4d-114">For more information about scripting for ADSI, see [Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).</span></span>

 

 




