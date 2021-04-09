---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968741"
---
# <a name="user-agent-string"></a><span data-ttu-id="9813e-103">Stringa agente utente</span><span class="sxs-lookup"><span data-stu-id="9813e-103">User Agent String</span></span>

<span data-ttu-id="9813e-104">La *stringa agente utente* contiene informazioni sull'identità di un browser.</span><span class="sxs-lookup"><span data-stu-id="9813e-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="9813e-105">La stringa agente utente viene segnalata al server Web come intestazione HTTP ogni volta che un browser esegue una richiesta a un server Web.</span><span class="sxs-lookup"><span data-stu-id="9813e-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="9813e-106">È anche possibile accedervi tramite uno script sul lato client.</span><span class="sxs-lookup"><span data-stu-id="9813e-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="9813e-107">Ad esempio, è possibile visualizzare la stringa agente utente digitando l'URL seguente nella barra degli indirizzi di Windows Internet Explorer 8: "JavaScript: Alert (Navigator. userAgent)".</span><span class="sxs-lookup"><span data-stu-id="9813e-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="9813e-108">Nell'illustrazione seguente viene mostrata la finestra di dialogo tipica risultante da Internet Explorer 8 in esecuzione in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9813e-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![screenshot della finestra di Internet Explorer diaog con la stringa agente utente](images/useragent-alert.png)

<span data-ttu-id="9813e-110">In genere, la stringa agente utente viene analizzata in modo specifico per la sottostringa MSIE.</span><span class="sxs-lookup"><span data-stu-id="9813e-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="9813e-111">In base alla versione segnalata del browser, la logica di programmazione lato client o lato server esegue un'azione diversa.</span><span class="sxs-lookup"><span data-stu-id="9813e-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="9813e-112">Per ulteriori informazioni sulla stringa agente utente, vedere [quali sono i report di Windows Internet Explorer come stringa di User-Agent?](/previous-versions/cc817582(v=msdn.10)) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="9813e-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9813e-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9813e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9813e-114">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="9813e-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



