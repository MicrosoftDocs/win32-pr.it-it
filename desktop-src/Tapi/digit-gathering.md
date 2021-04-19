---
description: Oltre ad abilitare il monitoraggio delle cifre e ricevere una notifica delle cifre una alla volta, un'applicazione può anche richiedere che vengano raccolte più cifre in un buffer.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Raccolta cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309961"
---
# <a name="digit-gathering"></a><span data-ttu-id="12d4d-103">Raccolta cifre</span><span class="sxs-lookup"><span data-stu-id="12d4d-103">Digit Gathering</span></span>

<span data-ttu-id="12d4d-104">Oltre ad abilitare il monitoraggio delle cifre e ricevere una notifica delle cifre una alla volta, un'applicazione può anche richiedere che vengano raccolte più cifre in un buffer.</span><span class="sxs-lookup"><span data-stu-id="12d4d-104">Besides enabling digit monitoring and being notified of digits one at a time, an application can also request that multiple digits be collected in a buffer.</span></span> <span data-ttu-id="12d4d-105">Solo quando il buffer è pieno o quando viene soddisfatta una determinata condizione di terminazione, l'applicazione riceve una notifica.</span><span class="sxs-lookup"><span data-stu-id="12d4d-105">Only when the buffer is full or when some other termination condition is met is the application notified.</span></span> <span data-ttu-id="12d4d-106">La raccolta di cifre è utile per le funzioni, ad esempio la raccolta dei numeri di carta di credito.</span><span class="sxs-lookup"><span data-stu-id="12d4d-106">Digit gathering is useful for functions such as credit card number collection.</span></span> <span data-ttu-id="12d4d-107">Viene eseguita quando un'applicazione chiama [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), specificando un buffer da riempire con le cifre.</span><span class="sxs-lookup"><span data-stu-id="12d4d-107">It is performed when an application calls [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), specifying a buffer to fill with digits.</span></span> <span data-ttu-id="12d4d-108">La raccolta di cifre termina quando viene soddisfatta una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="12d4d-108">Digit gathering terminates when one of the following conditions is true:</span></span>

-   <span data-ttu-id="12d4d-109">Il numero di cifre richiesto è stato raccolto.</span><span class="sxs-lookup"><span data-stu-id="12d4d-109">The requested number of digits has been collected.</span></span>
-   <span data-ttu-id="12d4d-110">È stata rilevata una o più cifre di terminazione.</span><span class="sxs-lookup"><span data-stu-id="12d4d-110">One of multiple termination digits is detected.</span></span> <span data-ttu-id="12d4d-111">Le cifre di terminazione vengono specificate per [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)e la cifra di chiusura viene inserita anche nel buffer.</span><span class="sxs-lookup"><span data-stu-id="12d4d-111">The termination digits are specified to [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), and the termination digit is placed in the buffer as well.</span></span>
-   <span data-ttu-id="12d4d-112">Uno dei due timeout scade.</span><span class="sxs-lookup"><span data-stu-id="12d4d-112">One of two timeouts expires.</span></span> <span data-ttu-id="12d4d-113">I timeout sono un timeout della prima cifra, che specifica la durata massima prima che la prima cifra debba essere raccolta e un timeout tra cifre, che specifica la durata massima tra le cifre successive.</span><span class="sxs-lookup"><span data-stu-id="12d4d-113">The timeouts are a first digit timeout, specifying the maximum duration before the first digit must be collected, and an inter-digit timeout, specifying the maximum duration between successive digits.</span></span>
-   <span data-ttu-id="12d4d-114">La raccolta di cifre viene annullata in modo esplicito da [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) di nuovo con un altro set di parametri per avviare una nuova richiesta di raccolta o usando un parametro di buffer a cifre **null** da annullare.</span><span class="sxs-lookup"><span data-stu-id="12d4d-114">Digit gathering is canceled explicitly by [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) again with either another set of parameters to start a new gathering request or by using a **NULL** digit buffer parameter to cancel.</span></span>

<span data-ttu-id="12d4d-115">Quando la raccolta di cifre termina per qualsiasi motivo, viene inviato un messaggio di [**riga \_ GATHERDIGITS**](line-gatherdigits.md) all'applicazione che ha richiesto la raccolta delle cifre.</span><span class="sxs-lookup"><span data-stu-id="12d4d-115">When digit gathering terminates for any reason, a [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is sent to the application that requested the digit gathering.</span></span> <span data-ttu-id="12d4d-116">In una chiamata in qualsiasi momento, in tutte le applicazioni proprietarie della chiamata, può essere in attesa una sola richiesta di raccolta con una sola cifra.</span><span class="sxs-lookup"><span data-stu-id="12d4d-116">Only a single digit gathering request can be outstanding on a call at any given time across all applications that are owners of the call.</span></span>

<span data-ttu-id="12d4d-117">La raccolta di cifre e il monitoraggio delle cifre possono essere abilitati nella stessa chiamata nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="12d4d-117">Digit gathering and digit monitoring can be enabled on the same call at the same time.</span></span> <span data-ttu-id="12d4d-118">In tal caso, l'applicazione riceverà un messaggio di [**riga \_ MONITORDIGITS**](line-monitordigits.md) per ogni cifra rilevata e un messaggio di riga separato \_ GATHERDIGITS quando il buffer viene restituito.</span><span class="sxs-lookup"><span data-stu-id="12d4d-118">In that case, the application will receive a [**LINE\_MONITORDIGITS**](line-monitordigits.md) message for each detected digit and a separate LINE\_GATHERDIGITS message when the buffer is sent back.</span></span>

 

 



