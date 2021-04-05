---
title: Gestione degli errori RAS
description: Quando si verifica un errore, la gestione connessione di accesso remoto richiama il gestore di notifiche del client.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS del servizio di accesso remoto, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712868"
---
# <a name="handling-ras-errors"></a><span data-ttu-id="52e2c-104">Gestione degli errori RAS</span><span class="sxs-lookup"><span data-stu-id="52e2c-104">Handling RAS Errors</span></span>

<span data-ttu-id="52e2c-105">Quando si verifica un errore, la gestione connessione di accesso remoto richiama il gestore di notifiche del client.</span><span class="sxs-lookup"><span data-stu-id="52e2c-105">When an error occurs, the Remote Access Connection Manager invokes the client's notification handler.</span></span> <span data-ttu-id="52e2c-106">La notifica indica lo stato della connessione quando si è verificato l'errore e un codice che identifica l'errore.</span><span class="sxs-lookup"><span data-stu-id="52e2c-106">The notification indicates the connection state when the error occurred, and a code that identifies the error.</span></span> <span data-ttu-id="52e2c-107">In questi casi, il gestore delle notifiche deve chiamare [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) per terminare la connessione RAS.</span><span class="sxs-lookup"><span data-stu-id="52e2c-107">In these cases, the notification handler should call [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) to end the RAS connection.</span></span>

<span data-ttu-id="52e2c-108">I codici di errore che identificano gli errori RAS sono definiti nel file raserror. h.</span><span class="sxs-lookup"><span data-stu-id="52e2c-108">The error codes that identify RAS errors are defined in the file raserror.h.</span></span> <span data-ttu-id="52e2c-109">Il client RAS può usare la funzione [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) per ottenere una stringa di visualizzazione che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="52e2c-109">The RAS client can use the [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) function to get a display string describing the error.</span></span> <span data-ttu-id="52e2c-110">Per una descrizione di questi errori, vedere [codici di errore di routing e accesso remoto](routing-and-remote-access-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="52e2c-110">See [Routing and Remote Access Error Codes](routing-and-remote-access-error-codes.md) for a description of these errors.</span></span>

 

 




