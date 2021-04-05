---
title: Gestione degli errori dell'applicazione server
description: Se l'applicazione server elabora correttamente il file caricato, l'applicazione deve restituire 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707855"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="732cc-103">Gestione degli errori dell'applicazione server</span><span class="sxs-lookup"><span data-stu-id="732cc-103">Handling Server Application Errors</span></span>

<span data-ttu-id="732cc-104">Se l'applicazione server elabora correttamente il file caricato, l'applicazione deve restituire 200.</span><span class="sxs-lookup"><span data-stu-id="732cc-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="732cc-105">Se l'applicazione non restituisce 200, il client BITS usa il codice di errore per determinare se l'errore è un errore temporaneo o un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="732cc-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="732cc-106">Tutti i codici di errore di 3xx sono errori temporanei tranne 300-305 e 307, che sono errori irreversibili.</span><span class="sxs-lookup"><span data-stu-id="732cc-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="732cc-107">Tutti i codici di errore di 4xx sono errori irreversibili ad eccezione di 408 e 409, che sono errori temporanei.</span><span class="sxs-lookup"><span data-stu-id="732cc-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="732cc-108">Tutti i codici di errore di 5xx sono errori temporanei tranne 501 e 505, che sono errori irreversibili.</span><span class="sxs-lookup"><span data-stu-id="732cc-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="732cc-109">Tutti gli altri codici HTTP sono considerati errori temporanei.</span><span class="sxs-lookup"><span data-stu-id="732cc-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="732cc-110">Si noti che un codice di errore 403 è l'unico codice di errore che impedisce a BITS di pubblicare nuovamente il file di caricamento nell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="732cc-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="732cc-111">Per recuperare l'errore, chiamare il metodo [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) .</span><span class="sxs-lookup"><span data-stu-id="732cc-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="732cc-112">Il contesto di errore sarà \_ applicazione remota del contesto di errore BG \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="732cc-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




