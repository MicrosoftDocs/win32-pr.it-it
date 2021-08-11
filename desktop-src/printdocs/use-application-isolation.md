---
description: Le app possono dichiarare l'isolamento del driver della stampante nel manifesto dell'app per isolare l'app dal driver della stampante e migliorare l'affidabilità delle app.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: "Procedura: Usare l'isolamento dell'applicazione"
ms.date: 05/31/2018
ms.openlocfilehash: 818ba30e7b294c695b2f67bb9bccc485959db43818bb95aedaa67cafc26d3559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233831"
---
# <a name="how-to-use-application-isolation"></a>Procedura: Usare l'isolamento dell'applicazione

Le app possono dichiarare l'isolamento del driver della stampante nel manifesto dell'app per isolare l'app dal driver della stampante e migliorare l'affidabilità dell'app. Il Windows di stampa consente l'esecuzione dei driver della stampante in processi separati dal processo in cui viene eseguito lo spooler di stampa. L'uso di questa funzionalità impedisce l'arresto anomalo dell'app nel caso in cui il driver della stampante presenti un errore.

L'isolamento del driver della stampante viene implementato in Windows 7 e Windows Server 2008 R2.

### <a name="prerequisites"></a>Prerequisiti

-   Codice gestito o app Windows Store che usa la Windows stampa.

## <a name="instructions"></a>Istruzioni

### <a name="update-the-app-manifest"></a>Aggiornare il manifesto dell'app

Per abilitare l'isolamento del driver della stampante è necessario aggiungere **l'elemento printerDriverIsolation** al manifesto dell'app. Ecco come:

1.  Modificare il manifesto dell'app aggiungendo l'elemento **printerDriverIsolation** con valore **true** all'elemento **windowsSettings** dell'elemento **dell'applicazione,** come illustrato in questo esempio.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Ricompilare l'app.

 

 



