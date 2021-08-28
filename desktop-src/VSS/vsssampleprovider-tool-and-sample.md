---
description: Illustra come usare le interfacce vss per creare un provider hardware vss.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Strumento e esempio vssSampleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd84288f6dc878c103f639aa0c015a3e5e95bde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884420"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Strumento e esempio vssSampleProvider

Illustra come usare le interfacce vss [per](volume-shadow-copy-api-interfaces.md) creare un provider hardware vss.

> [!Note]  
> Lo strumento VssSampleProvider e l'esempio sono inclusi in Microsoft Windows Software Development Kit (SDK). È possibile scaricare Windows SDK [da Windows Software Development Kit (SDK) per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

Nell'installazione di Windows SDK, lo strumento VssSampleProvider è disponibile in (per Windows a 64 bit) e (per le Windows `%Program Files(x86)%\Windows Kits\8.1\bin\x64` `%Program Files(x86)%\Windows Kits\8.1\bin\x86` a 32 bit).

> [!Note]  
> I provider di hardware sono supportati solo nei Windows server. In un Windows operativo client è possibile compilare l'esempio VssSampleProvider, ma non è possibile registrarlo come provider hardware.

 

Lo strumento VssSampleProvider è costituito dai file seguenti:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

L'esempio VssSampleProvider include gli script di installazione e disinstallazione seguenti:

-   Install-sampleprovider.cmd
-   Uninstall-sampleprovider.cmd
-   Registrare \_app.vbs

**Per installare e usare l'esempio VssSampleProvider**

1.  Passare alla directory `Program Files (x86)\Windows Kits\8.0\bin\`. Questa directory contiene virtualstoragevss.sys e vstorcontrol.exe.
2.  Aprire una finestra del prompt dei comandi nella directory specificata.
3.  Per installare il driver di archiviazione virtuale, nella finestra del prompt dei comandi digitare il comando seguente:

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Per installare il provider di esempio VSS, nella finestra del prompt dei comandi digitare il comando seguente:

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Per creare un LUN virtuale, eseguire le operazioni seguenti.

    1.  Nella finestra del prompt dei comandi digitare il comando seguente:

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Questo comando crea un LUN virtuale il cui identificatore di archiviazione è **VSS Sample HW Provider**. Per creare lun virtuali aggiuntivi, ripetere questo passaggio.

        Il provider di esempio VSS riconosce un LUN solo se il **provider HW di esempio vss** fa parte dell'identificatore di archiviazione. Per altre informazioni sull'identificatore di archiviazione, vedere il post di blog seguente.

        [LUN - Risincronizzazione con Diskshadow e virtual Archiviazione](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Nella finestra del prompt dei comandi usare diskpart.exe per formattare il disco virtuale e assegnare una lettera di unità.

        Ecco uno script di esempio da eseguire al prompt dei comandi diskpart.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Per eseguire il provider di esempio, nella finestra del prompt dei comandi digitare il comando seguente:

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *&lt; unità &gt;* rappresenta la lettera di unità del LUN virtuale.

7.  Per disinstallare il provider di esempio VSS, nella finestra del prompt dei comandi digitare il comando seguente:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Per disinstallare il driver di archiviazione virtuale, nella finestra del prompt dei comandi digitare il comando seguente:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



