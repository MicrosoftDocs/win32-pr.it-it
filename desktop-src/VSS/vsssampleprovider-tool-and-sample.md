---
description: Viene illustrato come utilizzare le interfacce VSS per creare un provider hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Strumento VssSampleProvider ed esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307140"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Strumento VssSampleProvider ed esempio

Viene illustrato come utilizzare le [interfacce](volume-shadow-copy-api-interfaces.md) VSS per creare un provider hardware VSS.

> [!Note]  
> Lo strumento e l'esempio VssSampleProvider sono inclusi nel Software Development Kit (SDK) di Microsoft Windows. È possibile scaricare il Windows SDK da [Windows Software Development Kit (SDK) per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

Nell'installazione di Windows SDK lo strumento VssSampleProvider si trova in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (per Windows a 64 bit) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (per windows a 32 bit).

> [!Note]  
> I provider hardware sono supportati solo nei sistemi operativi Windows Server. In un sistema operativo client Windows, è possibile compilare l'esempio VssSampleProvider, ma non è possibile registrarlo come provider hardware.

 

Lo strumento VssSampleProvider è costituito dai file seguenti:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

L'esempio VssSampleProvider include gli script di installazione e disinstallazione seguenti:

-   Install-SampleProvider. cmd
-   Uninstall-SampleProvider. cmd
-   Registra \_app.vbs

**Per installare e usare l'esempio VssSampleProvider**

1.  Passare alla directory `Program Files (x86)\Windows Kits\8.0\bin\`. Questa directory contiene virtualstoragevss.sys e vstorcontrol.exe.
2.  Aprire una finestra del prompt dei comandi nella directory specificata.
3.  Per installare il driver di archiviazione virtuale, digitare il comando seguente nella finestra del prompt dei comandi:

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

        

        Questo comando crea un LUN virtuale il cui identificatore di archiviazione è il **provider HW di esempio VSS**. Per creare LUN virtuali aggiuntivi, ripetere questo passaggio.

        Il provider di esempio VSS riconosce un LUN solo se il **provider HW di esempio VSS** fa parte dell'identificatore di archiviazione. Per ulteriori informazioni sull'identificatore di archiviazione, vedere il seguente post di Blog.

        [LUN-risincronizzazione con DiskShadow e archiviazione virtuale](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  Nella finestra del prompt dei comandi usare diskpart.exe per formattare il disco virtuale e assegnarvi una lettera di unità.

        Ecco uno script di esempio da eseguire al prompt dei comandi Diskpart.

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

    

    *<drive>* rappresenta la lettera di unità del LUN virtuale.

7.  Per disinstallare il provider di esempio VSS, nella finestra del prompt dei comandi digitare il comando seguente:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Per disinstallare il driver di archiviazione virtuale, digitare il comando seguente nella finestra del prompt dei comandi:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



