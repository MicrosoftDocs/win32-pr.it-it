---
description: L'API shell fornisce funzioni che è possibile usare per gestire le stampanti di rete. Se a un file è associato il verbo di stampa, è possibile usare il comando ShellExecuteEx per stamparlo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gestione delle stampanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979954"
---
# <a name="managing-printers"></a>Gestione delle stampanti

L'API shell fornisce funzioni che è possibile usare per gestire le stampanti di rete. Se a un file è associato il verbo di **stampa** , è possibile usare il comando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per stamparlo.

-   [Gestione stampanti](#printer-management)
-   [Stampa di file con ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Gestione stampanti

È possibile gestire le stampanti in un sistema con la funzione [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) . Questa funzione consente di:

-   Installare le stampanti.
-   Aprire stampanti.
-   Ottenere le proprietà della stampante.
-   Creare collegamenti alla stampante.
-   Stampare una pagina di prova.

## <a name="printing-files-with-shellexecuteex"></a>Stampa di file con ShellExecuteEx

Se a un tipo di file è associato un comando stampa, è possibile stampare il file chiamando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con **Print** come verbo. Questo comando è spesso identico a quello usato per il verbo **aperto** , con l'aggiunta di un flag per indicare all'applicazione di stampare il file. Ad esempio, i file con estensione txt possono essere stampati da Microsoft WordPad. Il verbo **Open** per un file con estensione txt corrisponderebbe quindi a un comando simile al seguente:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Quando si usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per stampare un file con estensione txt, WordPad apre il file, lo stampa e quindi lo chiude, restituendo il controllo all'applicazione. La funzione di esempio seguente accetta un percorso completo e USA **ShellExecuteEx** per stamparlo, usando il comando Print associato all'estensione del nome file.


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



