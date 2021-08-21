---
description: L'API Shell fornisce funzioni che è possibile usare per gestire le stampanti in rete. Se a un file è associato il verbo di stampa, è possibile usare il comando ShellExecuteEx per stamparlo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gestione delle stampanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7086b360355d0ad85be440bc8bc9e330bfa6dd25793cc943d3aacdbaa0d4a8f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719599"
---
# <a name="managing-printers"></a>Gestione delle stampanti

L'API Shell fornisce funzioni che è possibile usare per gestire le stampanti in rete. Se a un file è associato **il** verbo di stampa, è possibile usare il [**comando ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per stamparlo.

-   [Gestione delle stampanti](#printer-management)
-   [Stampa di file con ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Gestione delle stampanti

È possibile gestire le stampanti in un sistema con [**la funzione SHInvokePrinterCommand.**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) Questa funzione consente di:

-   Installare le stampanti.
-   Aprire le stampanti.
-   Ottenere le proprietà della stampante.
-   Creare collegamenti alla stampante.
-   Stampare una pagina di prova.

## <a name="printing-files-with-shellexecuteex"></a>Stampa di file con ShellExecuteEx

Se a un tipo di file è associato un comando print, è possibile stampare il file chiamando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) **con print** come verbo. Questo comando è spesso uguale a quello usato per il verbo **open,** con l'aggiunta di un flag per indicare all'applicazione di stampare il file. Ad esempio, .txt file possono essere stampati da Microsoft WordPad. Il **verbo** open per un .txt file corrisponderebbe quindi a qualcosa di simile al comando seguente:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



Quando si usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per stampare un file .txt, WordPad apre il file, lo stampa e quindi lo chiude, restituisce il controllo all'applicazione. La funzione di esempio seguente accetta un percorso completo e usa **ShellExecuteEx** per stamparlo, usando il comando print associato alla relativa estensione di file.


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



 

 



