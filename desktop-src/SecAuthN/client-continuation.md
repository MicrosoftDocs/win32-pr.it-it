---
description: Alcuni protocolli richiedono più messaggi di autenticazione.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuazione client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880514"
---
# <a name="client-continuation"></a><span data-ttu-id="1a31f-103">Continuazione client</span><span class="sxs-lookup"><span data-stu-id="1a31f-103">Client Continuation</span></span>

<span data-ttu-id="1a31f-104">Alcuni protocolli richiedono più messaggi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1a31f-104">Some protocols require multiple authentication messages.</span></span> <span data-ttu-id="1a31f-105">In questo caso, il client analizza la risposta dal server e chiama di nuovo [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) utilizzando lo stato continue della chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="1a31f-105">In this case, the client parses the response from the server and calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) again using the continue status from the previous call.</span></span> <span data-ttu-id="1a31f-106">Il client controlla lo stato di restituzione da questa chiamata e potrebbe essere necessario continuare per le gambe aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="1a31f-106">The client checks the return status from this call and might be required to continue for additional legs.</span></span> <span data-ttu-id="1a31f-107">Usa le informazioni contenute in *pOutput* per creare un messaggio e inviarlo al server.</span><span class="sxs-lookup"><span data-stu-id="1a31f-107">It uses the information in *pOutput* to construct a message and sends it to the server.</span></span>

 

 
