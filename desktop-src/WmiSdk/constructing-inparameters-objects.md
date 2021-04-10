---
description: Un oggetto InParameters contiene l'elenco di parametri per chiamare i metodi del provider quando si usa un tipo di chiamata ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Costruzione di oggetti InParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880678"
---
# <a name="constructing-inparameters-objects"></a>Costruzione di oggetti InParameters

Un oggetto [**InParameters**](swbemmethod-inparameters.md) contiene l'elenco di parametri per chiamare i metodi del provider quando si usa un tipo di chiamata **ExecMethod** . I metodi [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) richiedono un oggetto **InParameters** .

Nella procedura riportata di seguito viene descritto come costruire un oggetto [**InParameters**](swbemmethod-inparameters.md) .

**Per costruire il parametro *objwbemInParams***

1.  Connettersi a WMI.
2.  Ottenere la definizione della classe WMI che definisce il metodo che si desidera eseguire.
3.  Ottenere un oggetto [**InParameters**](swbemmethod-inparameters.md) specifico per il metodo della classe WMI che si desidera eseguire.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Impostare le proprietà dell'istanza su qualsiasi valore appropriato. Assicurarsi di assegnare valori alle proprietà chiave della classe WMI che contiene il metodo che si desidera eseguire.

    Se ad esempio si desidera impostare un parametro di input denominato myinputparam sul valore "ABC" in un'istanza di [**InParameters**](swbemmethod-inparameters.md) denominata "Inst", il codice sarà simile al seguente.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Eseguire il metodo e ottenere lo stato di restituzione del metodo in esecuzione.

Nell'esempio di codice seguente viene illustrata la configurazione dell'oggetto [**InParameters**](swbemmethod-inparameters.md) per creare un nuovo oggetto WMI che rappresenta una condivisione. Per ulteriori informazioni sull'oggetto [**OutParameters**](swbemmethod-outparameters.md) , vedere [analisi degli oggetti OutParameters](parsing-outparameters-objects.md). In questo esempio viene restituito un valore restituito con esito positivo (0) se è presente una cartella denominata "Share" nella posizione "C:/Share". Questo esempio consente di condividere la cartella con altri utenti.


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



