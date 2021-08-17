---
description: Un oggetto InParameters contiene l'elenco di parametri per chiamare i metodi del provider quando si usa un tipo di chiamata ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Costruzione di oggetti InParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc13a51687954331a050337fe785bab29b23ee9c72785ffde78d4f8a8e0d198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131583"
---
# <a name="constructing-inparameters-objects"></a>Costruzione di oggetti InParameters

Un [**oggetto InParameters**](swbemmethod-inparameters.md) contiene l'elenco di parametri per chiamare i metodi del provider quando si usa un tipo di chiamata **ExecMethod.** I [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md),SWbemObject.Exe [**cMethodAsync \_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)eSWbemServices.Exe [**cMethodAsync**](swbemservices-execmethodasync.md) richiedono tutti un **oggetto InParameters.**

La procedura seguente descrive come costruire un [**oggetto InParameters.**](swbemmethod-inparameters.md)

**Per costruire il *parametro objwbemInParams***

1.  Connessione a WMI.
2.  Ottenere la definizione della classe WMI che definisce il metodo da eseguire.
3.  Ottenere un [**oggetto InParameters**](swbemmethod-inparameters.md) specifico del metodo della classe WMI che si vuole eseguire.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Impostare le proprietà dell'istanza su tutti i valori appropriati. Assicurarsi di assegnare valori alle proprietà chiave nella classe WMI che contiene il metodo da eseguire.

    Ad esempio, se si vuole impostare un parametro di input denominato myinputparam sul valore "abc" in un'istanza di [**InParameters**](swbemmethod-inparameters.md) denominata "INST", il codice sarà simile al seguente.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Eseguire il metodo e ottenere lo stato restituito del metodo in esecuzione.

Nell'esempio di codice seguente viene illustrata la configurazione [**dell'oggetto InParameters**](swbemmethod-inparameters.md) per creare un nuovo oggetto WMI che rappresenta una condivisione. Per altre informazioni [**sull'oggetto OutParameters,**](swbemmethod-outparameters.md) vedere [Parsing OutParameters Objects](parsing-outparameters-objects.md). In questo esempio viene restituito un valore restituito corretto (0) se è presente una cartella denominata "Share" nel percorso "C:/Share". Questo esempio consente di condividere questa cartella con altri utenti.


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



 

 



