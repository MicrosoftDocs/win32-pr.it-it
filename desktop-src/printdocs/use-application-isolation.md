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
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="fc929-103">Procedura: usare l'isolamento delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="fc929-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="fc929-104">Le app possono dichiarare l'isolamento dei driver della stampante nel manifesto dell'applicazione per isolare l'app dal driver della stampante e migliorare l'affidabilità dell'app.</span><span class="sxs-lookup"><span data-stu-id="fc929-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="fc929-105">Il servizio di stampa di Windows consente ai driver della stampante di essere eseguiti in processi distinti dal processo in cui viene eseguito lo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="fc929-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="fc929-106">Usando questa funzionalità, l'app impedisce l'arresto anomalo nel caso in cui il driver della stampante si sia verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="fc929-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="fc929-107">L'isolamento del driver della stampante viene implementato in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fc929-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fc929-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="fc929-108">Prerequisites</span></span>

-   <span data-ttu-id="fc929-109">Un'app di Windows Store o di codice gestito che usa la stampa di Windows.</span><span class="sxs-lookup"><span data-stu-id="fc929-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="fc929-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="fc929-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="fc929-111">Aggiornare il manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fc929-111">Update the app manifest</span></span>

<span data-ttu-id="fc929-112">Per abilitare l'isolamento dei driver della stampante, è necessario aggiungere l'elemento **printerDriverIsolation** al manifesto dell'app.</span><span class="sxs-lookup"><span data-stu-id="fc929-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="fc929-113">Ecco come:</span><span class="sxs-lookup"><span data-stu-id="fc929-113">Here's how:</span></span>

1.  <span data-ttu-id="fc929-114">Modificare il manifesto dell'applicazione, aggiungendo l'elemento **printerDriverIsolation** con un valore **true** all'elemento **windowsSettings** dell'elemento **Application** , come illustrato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="fc929-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="fc929-115">Ricompilare l'app.</span><span class="sxs-lookup"><span data-stu-id="fc929-115">Rebuild your app.</span></span>

 

 



