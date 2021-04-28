---
description: Stringa agente utente
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084179"
---
# <a name="user-agent-string"></a><span data-ttu-id="3dbc8-103">Stringa agente utente</span><span class="sxs-lookup"><span data-stu-id="3dbc8-103">User Agent String</span></span>

<span data-ttu-id="3dbc8-104">La *stringa agente utente* contiene informazioni sull'identità di un browser.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="3dbc8-105">La stringa agente utente viene segnalata al server Web come intestazione HTTP ogni volta che un browser effettua una richiesta a un server Web.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="3dbc8-106">È anche possibile accedervi tramite uno script sul lato client.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="3dbc8-107">Ad esempio, è possibile visualizzare la stringa agente utente digitando l'URL seguente nella barra degli indirizzi di Windows Internet Explorer 8: "javascript:alert(navigator.userAgent)".</span><span class="sxs-lookup"><span data-stu-id="3dbc8-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="3dbc8-108">La figura seguente mostra la tipica finestra di dialogo risultante Internet Explorer 8 in esecuzione in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![Screenshot della casella del diaog di Internet Explorer con la stringa dell'agente utente](images/useragent-alert.png)

<span data-ttu-id="3dbc8-110">In genere, la stringa agente utente viene analizzata in modo specifico per la sottostringa MSIE.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="3dbc8-111">In base alla versione segnalata del browser, la logica di programmazione lato client o lato server richiede un'azione diversa.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="3dbc8-112">Per altre informazioni sulla stringa agente utente, vedere What [Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="3dbc8-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dbc8-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3dbc8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dbc8-114">Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità</span><span class="sxs-lookup"><span data-stu-id="3dbc8-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



