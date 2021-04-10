---
description: Le app possono dichiarare l'isolamento dei driver della stampante nel manifesto dell'applicazione per isolare l'app dal driver della stampante e migliorare l'affidabilità delle app.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: "Procedura: usare l'isolamento delle applicazioni"
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227459"
---
# <a name="how-to-use-application-isolation"></a>Procedura: usare l'isolamento delle applicazioni

Le app possono dichiarare l'isolamento dei driver della stampante nel manifesto dell'applicazione per isolare l'app dal driver della stampante e migliorare l'affidabilità dell'app. Il servizio di stampa di Windows consente ai driver della stampante di essere eseguiti in processi distinti dal processo in cui viene eseguito lo spooler di stampa. Usando questa funzionalità, l'app impedisce l'arresto anomalo nel caso in cui il driver della stampante si sia verificato un errore.

L'isolamento del driver della stampante viene implementato in Windows 7 e Windows Server 2008 R2.

### <a name="prerequisites"></a>Prerequisiti

-   Un'app di Windows Store o di codice gestito che usa la stampa di Windows.

## <a name="instructions"></a>Istruzioni

### <a name="update-the-app-manifest"></a>Aggiornare il manifesto dell'applicazione

Per abilitare l'isolamento dei driver della stampante, è necessario aggiungere l'elemento **printerDriverIsolation** al manifesto dell'app. Ecco come:

1.  Modificare il manifesto dell'applicazione, aggiungendo l'elemento **printerDriverIsolation** con un valore **true** all'elemento **windowsSettings** dell'elemento **Application** , come illustrato in questo esempio.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Ricompilare l'app.

 

 



