---
description: L'oggetto di scripting SWbemObject è l'oggetto WMI generico, che definisce proprietà e metodi che possono essere utilizzati indipendentemente dall'oggetto WMI specifico a cui è associato l'oggetto SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Creazione di script con SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131007"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="1e9cc-103">Creazione di script con SWbemObject</span><span class="sxs-lookup"><span data-stu-id="1e9cc-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="1e9cc-104">L'oggetto di scripting [**SWbemObject**](swbemobject.md) è l'oggetto WMI generico, che definisce proprietà e metodi che possono essere utilizzati indipendentemente dall'oggetto WMI specifico a cui è associato l'oggetto **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="1e9cc-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="1e9cc-105">Tutti gli oggetti WMI, ad esempio un'istanza [**del \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) o qualsiasi altra classe di dati WMI, sono rappresentati da [**SWbemObject**](swbemobject.md) e possono utilizzare le proprietà e i metodi comuni di **SWbemObject** , oltre alle proprietà e ai metodi specifici.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="1e9cc-106">Usare, ad esempio, lo script seguente per ottenere tutte le istanze di un [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) chiamando il metodo [**SWbemObject. instances \_**](swbemobject-instances-.md) .</span><span class="sxs-lookup"><span data-stu-id="1e9cc-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="1e9cc-107">ClsobjProcess rappresenta sia la definizione della classe di **\_ processo Win32** sia una [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="1e9cc-108">Nell'esempio seguente viene ottenuta un'istanza specifica [**del \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) che rappresenta il servizio Alerter e la archivia in objAlerter.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="1e9cc-109">È quindi possibile chiamare i metodi [**SWbemObject**](swbemobject.md) , ad esempio WScript. Echo ObjAlerter. Path \_ , o i metodi definiti dalla classe di dati, ad esempio WScript. Echo objAlerter. state.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="1e9cc-110">objAlerter che rappresenta un'istanza del servizio Win32 \_ e un **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="1e9cc-111">La chiamata a [**SWbemObject. instances \_**](swbemobject-instances-.md) ottiene un altro oggetto generico di script WMI, [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="1e9cc-112">Come illustrato, l'oggetto **SWbemObjectSet** può essere considerato come una [raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="1e9cc-113">È possibile identificare i metodi [**SWbemObject**](swbemobject.md) perché tutti terminano con un carattere di sottolineatura ( \_ ), ad esempio [**SWbemObject \_ . Instances**](swbemobject-instances-.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="1e9cc-114">[**SWbemObjectEx**](swbemobjectex.md) estende le proprietà di [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="1e9cc-115">Ad esempio, è ora possibile aggiornare i dati di qualsiasi oggetto WMI, ad esempio un'istanza del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process), mediante una chiamata a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="1e9cc-116">Nell'esempio seguente viene illustrato come i dati di errore della pagina processo di sistema possono essere aggiornati ogni cinque secondi.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="1e9cc-117">Per ulteriori informazioni sull'aggiornamento dei dati tramite un oggetto [**SWbemRefresher**](swbemrefresher.md) , vedere [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="1e9cc-118">[**SWbemObject. put \_**](swbemobject-put-.md) e [**PutAsync \_**](swbemobject-putasync-.md) consentono di scrivere di nuovo le modifiche in qualsiasi oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="1e9cc-119">Questi metodi consentono di eseguire il commit delle modifiche a un oggetto nello spazio dei nomi in cui è stato creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1e9cc-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="1e9cc-120">È possibile scrivere l'oggetto in uno spazio dei nomi diverso usando [**SWbemServicesEx. Put**](swbemservicesex-put.md) o [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).</span><span class="sxs-lookup"><span data-stu-id="1e9cc-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e9cc-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e9cc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e9cc-122">API di scripting per WMI</span><span class="sxs-lookup"><span data-stu-id="1e9cc-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="1e9cc-123">Creazione di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="1e9cc-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="1e9cc-124">Aggiornamento di un'intera istanza</span><span class="sxs-lookup"><span data-stu-id="1e9cc-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="1e9cc-125">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="1e9cc-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
