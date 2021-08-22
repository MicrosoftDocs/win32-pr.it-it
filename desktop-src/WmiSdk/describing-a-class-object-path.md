---
description: Il percorso di un oggetto classe descrive la posizione di una classe all'interno di uno spazio dei nomi.
ms.assetid: 5ae95707-d023-4102-9b41-140c54b0c5b7
ms.tgt_platform: multiple
title: Descrizione del percorso di un oggetto classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6801d91c4236a7892d7db121dc02c73d93640b7dbc4969c86db55a8789b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244401"
---
# <a name="describing-a-class-object-path"></a>Descrizione del percorso di un oggetto classe

Il percorso di un oggetto classe descrive la posizione di una classe all'interno di uno spazio dei nomi.

È possibile usare i metodi seguenti per specificare il percorso di un oggetto:

-   Un percorso completo dell'oggetto a una classe aggiunge il nome della classe a un percorso dello spazio dei nomi.

    L'esempio seguente illustra il percorso della [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) all'interno dello spazio dei nomi \\ cimv2 radice nel \\ server denominato Admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Un percorso di oggetto relativo rappresenta una classe che risiede nello spazio dei nomi corrente. Un percorso di oggetto relativo a una classe contiene solo il nome della classe.

    Nell'esempio seguente viene illustrato il percorso relativo della [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

    ``` syntax
    Win32_LogicalDisk
    ```

Quando si esegue una query per un nome di classe ma non si specifica alcuna istanza, WMI restituisce la definizione della classe. La procedura seguente descrive come recuperare una definizione di classe in VBScript.

**Per recuperare una definizione di classe in VBScript**

-   È possibile usare la connessione del moniker con una query o [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx). È anche possibile usare [**SWbemServices.Get**](swbemservices-get.md).

    Nell'esempio seguente viene illustrato come usare [GetObject](/previous-versions//kdccchxa(v=vs.85)) per ottenere una definizione di classe.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
       & "{impersonationLevel=impersonate}!\\" _
       & strComputer & "\root\cimv2:Win32_Printer")
    ```

    

    Nell'esempio seguente viene illustrato come eseguire una query per una definizione di classe.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:" _
        & "{impersonationLevel=impersonate}!\\" _
        & strComputer & "\root\cimv2")
    Set colInstalledPrinters =  objWMIService.ExecQuery _
        ("Select * from Win32_Printer")
    ```

    

È possibile recuperare una definizione di classe in C++ specificando solo il nome della classe e nessun percorso per una determinata istanza. La procedura seguente descrive come recuperare una definizione di classe in C++.

**Per recuperare una definizione di classe in C++**

-   Effettuare una chiamata alle [**funzioni IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    L'esempio seguente illustra come chiamare la [**funzione IWbemServices::GetObject.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    L'esempio di codice precedente richiede la corretta \# compilazione dell'istruzione include seguente.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
