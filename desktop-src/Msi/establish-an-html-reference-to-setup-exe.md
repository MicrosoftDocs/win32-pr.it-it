---
description: Il passaggio finale consiste nell'inserire un riferimento al Setup.exe nella pagina Web ipotetica di configurazione (MySetup.html) descritta in un esempio di installazione Windows Installer basato su URL.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Definire un riferimento HTML a Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231873"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="690a5-103">Definire un riferimento HTML a Setup.exe</span><span class="sxs-lookup"><span data-stu-id="690a5-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="690a5-104">Il passaggio finale consiste nell'inserire un riferimento al Setup.exe nella pagina Web ipotetica di configurazione (MySetup.html) descritta in [un esempio di installazione Windows Installer basato su URL](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="690a5-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="690a5-105">Usare lo script HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="690a5-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="690a5-106">Facendo clic sul collegamento "installazione di configurazione" si presenta agli utenti l'opzione per salvare o eseguire da tale percorso.</span><span class="sxs-lookup"><span data-stu-id="690a5-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="690a5-107">Se l'utente seleziona Esegui da tale posizione, il Setup.exe aggiorna la versione di Windows Installer nel computer, se necessario, verifica la firma digitale nel pacchetto di installazione e installa il pacchetto nel computer.</span><span class="sxs-lookup"><span data-stu-id="690a5-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="690a5-108">Questa operazione completa l'esempio.</span><span class="sxs-lookup"><span data-stu-id="690a5-108">This completes the example.</span></span>

 

 



