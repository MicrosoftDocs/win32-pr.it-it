---
title: Formato driver installabile
description: Formato driver installabile
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- driver installabili, formati
- driver installabili, funzione DriverProc
- driver installabili, messaggi
- messaggi driver
- formati di driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337238"
---
# <a name="installable-driver-format"></a><span data-ttu-id="a738d-108">Formato driver installabile</span><span class="sxs-lookup"><span data-stu-id="a738d-108">Installable Driver Format</span></span>

<span data-ttu-id="a738d-109">Ogni driver installabile esporta una funzione [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) .</span><span class="sxs-lookup"><span data-stu-id="a738d-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="a738d-110">Questa funzione di punto di ingresso comune riceve *i messaggi del driver* dal sistema che indirizzano il driver a eseguire azioni o fornire informazioni.</span><span class="sxs-lookup"><span data-stu-id="a738d-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="a738d-111">Il sistema invia messaggi di driver alla funzione **DriverProc** quando un'applicazione o una DLL apre o chiude il driver o richiede che un messaggio venga inviato al driver.</span><span class="sxs-lookup"><span data-stu-id="a738d-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="a738d-112">La funzione **DriverProc** elabora il messaggio o passa il messaggio al gestore di messaggi predefinito, ovvero la funzione [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="a738d-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="a738d-113">In entrambi i casi, **DriverProc** deve restituire un valore che indica se l'azione richiesta è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="a738d-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 