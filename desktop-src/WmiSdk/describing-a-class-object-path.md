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
# <a name="describing-a-class-object-path"></a>Descrizione del percorso di un oggetto classe

Un percorso dell'oggetto classe descrive il percorso di una classe all'interno di uno spazio dei nomi.

Per specificare il percorso di un oggetto, è possibile usare i metodi seguenti:

-   Un percorso completo dell'oggetto a una classe aggiunge il nome della classe a un percorso dello spazio dei nomi.

    Nell'esempio seguente viene illustrata la posizione della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ \\ spazio dei nomi Cimv2 radice sul server denominato admin.

    ``` syntax
    \\Admin\Root\CimV2:Win32_LogicalDisk
    ```

-   Un percorso di oggetto relativo rappresenta una classe che risiede nello spazio dei nomi corrente. Il percorso di un oggetto relativo a una classe contiene solo il nome della classe.

    Nell'esempio seguente viene illustrato il percorso relativo della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

    ``` syntax
    Win32_LogicalDisk
    ```

Quando si esegue una query per un nome di classe ma non si specifica alcuna istanza, WMI restituisce la definizione della classe. Nella procedura riportata di seguito viene descritto come recuperare una definizione di classe in VBScript.

**Per recuperare una definizione di classe in VBScript**

-   È possibile utilizzare la connessione moniker con una query o un [**oggetto GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx). È anche possibile usare [**SWbemServices. Get**](swbemservices-get.md).

    Nell'esempio seguente viene illustrato come utilizzare [GetObject](/previous-versions//kdccchxa(v=vs.85)) per ottenere una definizione di classe.

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

    

È possibile recuperare una definizione di classe in C++ specificando solo il nome della classe e nessun percorso di una particolare istanza. Nella procedura riportata di seguito viene descritto come recuperare una definizione di classe in C++.

**Per recuperare una definizione di classe in C++**

-   Effettuare una chiamata alle funzioni [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    Nell'esempio seguente viene illustrato come chiamare la funzione [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .

    ```C++
    IWbemServices* pSvcs = 0;

    BSTR Path = SysAllocString(L"Win32_LogicalDisk");
    IWbemClassObject *pDiskClass = 0;
    pSvcs->GetObject(Path, 0, 0, &pDiskClass, 0);
    ```

    

    Nell'esempio di codice precedente è necessario \# che l'istruzione include seguente venga compilata correttamente.

    ```C++
    #include <wbemidl.h>
    ```

    

 

 
