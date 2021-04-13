---
description: Un percorso dell'oggetto istanza descrive il percorso di un'istanza di una determinata classe in uno spazio dei nomi specifico.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Descrizione del percorso di un oggetto istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347046"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="a8a7f-103">Descrizione del percorso di un oggetto istanza</span><span class="sxs-lookup"><span data-stu-id="a8a7f-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="a8a7f-104">Un percorso dell'oggetto istanza descrive il percorso di un'istanza di una determinata classe in uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="a8a7f-105">È possibile disporre di diversi tipi di percorsi degli oggetti di istanza:</span><span class="sxs-lookup"><span data-stu-id="a8a7f-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="a8a7f-106">Full</span><span class="sxs-lookup"><span data-stu-id="a8a7f-106">Full</span></span>

    <span data-ttu-id="a8a7f-107">Un percorso completo dell'oggetto istanza aggiunge il nome e il valore della proprietà chiave per la classe a un percorso completo dell'oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="a8a7f-108">Nell'esempio seguente viene illustrata la definizione del percorso completo dell'oggetto istanza.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="a8a7f-109">Relativo</span><span class="sxs-lookup"><span data-stu-id="a8a7f-109">Relative</span></span>

    <span data-ttu-id="a8a7f-110">Un percorso di oggetto relativo fa riferimento a un'istanza di che si trova nello spazio dei nomi corrente nel server corrente.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="a8a7f-111">Il percorso relativo è costituito dal nome della classe seguito dai nomi e dai valori delle proprietà chiave di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="a8a7f-112">Nell'esempio seguente viene illustrata la definizione del percorso dell'oggetto istanza relativo.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="a8a7f-113">Relativo con una singola chiave</span><span class="sxs-lookup"><span data-stu-id="a8a7f-113">Relative with a single key</span></span>

    <span data-ttu-id="a8a7f-114">Per le classi con una sola proprietà designata come chiave, è possibile omettere il nome della proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="a8a7f-115">Nell'esempio seguente viene illustrata la definizione del percorso dell'oggetto istanza relativo con una singola chiave.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="a8a7f-116">Relativa a più chiavi</span><span class="sxs-lookup"><span data-stu-id="a8a7f-116">Relative with multiple keys</span></span>

    <span data-ttu-id="a8a7f-117">Utilizzare una virgola per distinguere tra le chiavi di un'istanza con più chiavi.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="a8a7f-118">Nell'esempio seguente vengono illustrate le definizioni del percorso dell'oggetto istanza relativo con più chiavi.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="a8a7f-119">Relativo per una classe singleton</span><span class="sxs-lookup"><span data-stu-id="a8a7f-119">Relative for a singleton class</span></span>

    <span data-ttu-id="a8a7f-120">Il percorso dell'oggetto relativo per una classe singleton è costituito dal nome della classe seguito dalla notazione "= @".</span><span class="sxs-lookup"><span data-stu-id="a8a7f-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="a8a7f-121">Nell'esempio seguente viene illustrata la definizione del percorso dell'oggetto istanza relativo per una classe singleton.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="a8a7f-122">Nella procedura riportata di seguito viene descritto come recuperare un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="a8a7f-123">**Per recuperare un'istanza di classe**</span><span class="sxs-lookup"><span data-stu-id="a8a7f-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="a8a7f-124">Inizializza una stringa che contiene il percorso dell'oggetto con una chiamata alla funzione [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .</span><span class="sxs-lookup"><span data-stu-id="a8a7f-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="a8a7f-125">Inizializzare un oggetto che riceverà l'istanza.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="a8a7f-126">Recuperare l'oggetto con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="a8a7f-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="a8a7f-127">Per usare [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), è necessario implementare l'interfaccia [**IWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a7f-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="a8a7f-128">La seguente \# istruzione include è obbligatoria per il codice elencato più avanti in questo argomento per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="a8a7f-129">Nell'esempio di codice seguente viene illustrato come recuperare un'istanza della classe utilizzando un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="a8a7f-130">Per le istanze di classi che specificano più proprietà come chiave, WMI non richiede alcun ordinamento specifico delle proprietà chiave nei percorsi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="a8a7f-131">È necessario specificare solo il valore di ogni proprietà nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="a8a7f-132">Nell'esempio di codice seguente vengono descritte due descrizioni di chiave equivalenti.</span><span class="sxs-lookup"><span data-stu-id="a8a7f-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
