---
description: Un percorso dell'oggetto classe descrive il percorso di una classe all'interno di uno spazio dei nomi.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Descrizione del percorso di un oggetto classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfd603ea3b6de151d297a7f4b6fc8a2a27dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315731"
---
# <a name="describing-a-class-object-path"></a><span data-ttu-id="32fcc-103">Descrizione del percorso di un oggetto classe</span><span class="sxs-lookup"><span data-stu-id="32fcc-103">Describing a Class Object Path</span></span>

<span data-ttu-id="32fcc-104">Un percorso dell'oggetto classe descrive il percorso di una classe all'interno di uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32fcc-104">A class object path describes the location of a class within a namespace.</span></span>

<span data-ttu-id="32fcc-105">Per specificare il percorso di un oggetto, è possibile usare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="32fcc-105">You can use the following methods to specify an object path:</span></span>

-   <span data-ttu-id="32fcc-106">Un percorso completo dell'oggetto a una classe aggiunge il nome della classe a un percorso dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32fcc-106">A full object path to a class appends the class name to a namespace path.</span></span>

    <span data-ttu-id="32fcc-107">Nell'esempio seguente viene illustrata la posizione della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ \\ spazio dei nomi Cimv2 radice sul server denominato admin.</span><span class="sxs-lookup"><span data-stu-id="32fcc-107">The following example shows the location of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class within the \\root\\cimv2 namespace on the server named Admin.</span></span>

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   <span data-ttu-id="32fcc-108">Un percorso di oggetto relativo rappresenta una classe che risiede nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="32fcc-108">A relative object path represents a class that resides in the current namespace.</span></span> <span data-ttu-id="32fcc-109">Il percorso di un oggetto relativo a una classe contiene solo il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="32fcc-109">A relative object path to a class contains only the class name.</span></span>

    <span data-ttu-id="32fcc-110">Nell'esempio seguente viene illustrato il percorso relativo della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="32fcc-110">The following example shows the relative path to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

    ``` syntax
    Win32_LogicalDisk
    ```

<span data-ttu-id="32fcc-111">Quando si esegue una query per un nome di classe ma non si specifica alcuna istanza, WMI restituisce la definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="32fcc-111">When you query for a class name but specify no instances, WMI returns the class definition.</span></span> <span data-ttu-id="32fcc-112">Nella procedura riportata di seguito viene descritto come recuperare una definizione di classe in VBScript.</span><span class="sxs-lookup"><span data-stu-id="32fcc-112">The following procedure describes how to retrieve a class definition in VBScript.</span></span>

<span data-ttu-id="32fcc-113">**Per recuperare una definizione di classe in VBScript**</span><span class="sxs-lookup"><span data-stu-id="32fcc-113">**To retrieve a class definition in VBScript**</span></span>

-   <span data-ttu-id="32fcc-114">È possibile utilizzare la connessione moniker con una query o un [**oggetto GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="32fcc-114">You can use the moniker connection either with a query or [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx).</span></span> <span data-ttu-id="32fcc-115">È anche possibile usare [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="32fcc-115">You can also use [**SWbemServices.Get**](swbemservices-get.md).</span></span>

    <span data-ttu-id="32fcc-116">Nell'esempio seguente viene illustrato come utilizzare [GetObject](/previous-versions//kdccchxa(v=vs.85)) per ottenere una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="32fcc-116">The following example shows how to use [GetObject](/previous-versions//kdccchxa(v=vs.85)) to get a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    <span data-ttu-id="32fcc-117">Nell'esempio seguente viene illustrato come eseguire una query per una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="32fcc-117">The following example shows how to query for a class definition.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

<span data-ttu-id="32fcc-118">È possibile recuperare una definizione di classe in C++ specificando solo il nome della classe e nessun percorso di una particolare istanza.</span><span class="sxs-lookup"><span data-stu-id="32fcc-118">You can retrieve a class definition in C++ by specifying only the class name and no path to a particular instance.</span></span> <span data-ttu-id="32fcc-119">Nella procedura riportata di seguito viene descritto come recuperare una definizione di classe in C++.</span><span class="sxs-lookup"><span data-stu-id="32fcc-119">The following procedure describes how to retrieve a class definition in C++.</span></span>

<span data-ttu-id="32fcc-120">**Per recuperare una definizione di classe in C++**</span><span class="sxs-lookup"><span data-stu-id="32fcc-120">**To retrieve a class definition in C++**</span></span>

-   <span data-ttu-id="32fcc-121">Effettuare una chiamata alle funzioni [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="32fcc-121">Make a call to the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) functions.</span></span>

    <span data-ttu-id="32fcc-122">Nell'esempio seguente viene illustrato come chiamare la funzione [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="32fcc-122">The following example shows how to call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) function.</span></span>

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    <span data-ttu-id="32fcc-123">Nell'esempio di codice precedente è necessario \# che l'istruzione include seguente venga compilata correttamente.</span><span class="sxs-lookup"><span data-stu-id="32fcc-123">The previous code example requires the following \#include statement to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
