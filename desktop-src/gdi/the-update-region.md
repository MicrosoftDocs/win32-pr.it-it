---
description: L'area di aggiornamento identifica la parte di una finestra non aggiornata o non valida e che deve essere ridisegnata.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995093"
---
# <a name="the-update-region"></a><span data-ttu-id="4c36a-103">Area di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4c36a-103">The Update Region</span></span>

<span data-ttu-id="4c36a-104">L' *area di aggiornamento* identifica la parte di una finestra non aggiornata o non valida e che deve essere ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="4c36a-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="4c36a-105">Il sistema usa l'area di aggiornamento per generare messaggi di [**\_ disegno WM**](wm-paint.md) per le applicazioni e per ridurre al minimo il tempo impiegato dalle applicazioni per rendere aggiornato il contenuto delle finestre.</span><span class="sxs-lookup"><span data-stu-id="4c36a-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="4c36a-106">Il sistema aggiunge solo la parte non valida della finestra all'area di aggiornamento, richiedendo la traccia solo di tale parte.</span><span class="sxs-lookup"><span data-stu-id="4c36a-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="4c36a-107">Quando il sistema determina che è necessario aggiornare una finestra, imposta le dimensioni dell'area di aggiornamento sulla parte non valida della finestra.</span><span class="sxs-lookup"><span data-stu-id="4c36a-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="4c36a-108">L'impostazione dell'area di aggiornamento non comporta immediatamente il progetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c36a-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="4c36a-109">Al contrario, l'applicazione continua a recuperare i messaggi dalla coda di messaggi dell'applicazione fino a quando non restano messaggi.</span><span class="sxs-lookup"><span data-stu-id="4c36a-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="4c36a-110">Il sistema controlla quindi l'area di aggiornamento e, se l'area non è vuota (non NULL), invia un messaggio [**di \_ disegno WM**](wm-paint.md) alla routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="4c36a-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="4c36a-111">Un'applicazione può usare l'area di aggiornamento per generare i messaggi di [**\_ disegno WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="4c36a-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="4c36a-112">Ad esempio, un'applicazione che carica i dati da file aperti in genere imposta l'area di aggiornamento durante il caricamento in modo da disegnare nuovi dati durante l'elaborazione del messaggio di **\_ disegno WM** successivo.</span><span class="sxs-lookup"><span data-stu-id="4c36a-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="4c36a-113">In generale, un'applicazione non deve attingere al momento della modifica dei dati, ma instradare tutte le operazioni di disegno tramite il messaggio di disegno **WM \_** .</span><span class="sxs-lookup"><span data-stu-id="4c36a-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



