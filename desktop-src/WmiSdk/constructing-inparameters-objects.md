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
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="a364f-103">Costruzione di oggetti InParameters</span><span class="sxs-lookup"><span data-stu-id="a364f-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="a364f-104">Un oggetto [**InParameters**](swbemmethod-inparameters.md) contiene l'elenco di parametri per chiamare i metodi del provider quando si usa un tipo di chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="a364f-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="a364f-105">I metodi [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) richiedono un oggetto **InParameters** .</span><span class="sxs-lookup"><span data-stu-id="a364f-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="a364f-106">Nella procedura riportata di seguito viene descritto come costruire un oggetto [**InParameters**](swbemmethod-inparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="a364f-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="a364f-107">**Per costruire il parametro *objwbemInParams***</span><span class="sxs-lookup"><span data-stu-id="a364f-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="a364f-108">Connettersi a WMI.</span><span class="sxs-lookup"><span data-stu-id="a364f-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="a364f-109">Ottenere la definizione della classe WMI che definisce il metodo che si desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="a364f-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="a364f-110">Ottenere un oggetto [**InParameters**](swbemmethod-inparameters.md) specifico per il metodo della classe WMI che si desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="a364f-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="a364f-111">Impostare le proprietà dell'istanza su qualsiasi valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="a364f-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="a364f-112">Assicurarsi di assegnare valori alle proprietà chiave della classe WMI che contiene il metodo che si desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="a364f-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="a364f-113">Se ad esempio si desidera impostare un parametro di input denominato myinputparam sul valore "ABC" in un'istanza di [**InParameters**](swbemmethod-inparameters.md) denominata "Inst", il codice sarà simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="a364f-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="a364f-114">Eseguire il metodo e ottenere lo stato di restituzione del metodo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a364f-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="a364f-115">Nell'esempio di codice seguente viene illustrata la configurazione dell'oggetto [**InParameters**](swbemmethod-inparameters.md) per creare un nuovo oggetto WMI che rappresenta una condivisione.</span><span class="sxs-lookup"><span data-stu-id="a364f-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="a364f-116">Per ulteriori informazioni sull'oggetto [**OutParameters**](swbemmethod-outparameters.md) , vedere [analisi degli oggetti OutParameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a364f-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="a364f-117">In questo esempio viene restituito un valore restituito con esito positivo (0) se è presente una cartella denominata "Share" nella posizione "C:/Share".</span><span class="sxs-lookup"><span data-stu-id="a364f-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="a364f-118">Questo esempio consente di condividere la cartella con altri utenti.</span><span class="sxs-lookup"><span data-stu-id="a364f-118">This example enables this folder to be shared with other users.</span></span>


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



 

 



