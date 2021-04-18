---
description: Le operazioni di completamento consentono a un'applicazione di specificare come si desidera gestire una sessione quando fattori quali una destinazione occupata impediscono la connessione normale.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Completare una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308310"
---
# <a name="complete-a-session"></a><span data-ttu-id="1743f-103">Completare una sessione</span><span class="sxs-lookup"><span data-stu-id="1743f-103">Complete a Session</span></span>

<span data-ttu-id="1743f-104">Le operazioni di completamento consentono a un'applicazione di specificare come si desidera gestire una sessione quando fattori quali una destinazione occupata impediscono la connessione normale.</span><span class="sxs-lookup"><span data-stu-id="1743f-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="1743f-105">Le [ \_ costanti LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definiscono le possibili opzioni che possono avere un'applicazione, a seconda delle funzionalità del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="1743f-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="1743f-106">Più richieste di completamento delle chiamate potrebbero essere in attesa per un determinato indirizzo in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="1743f-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="1743f-107">Per identificare le singole richieste, l'implementazione restituisce un [identificatore di completamento](completion-id-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="1743f-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="1743f-108">L'annullamento di una richiesta di completamento delle chiamate in corso usa anche questo identificatore di completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="1743f-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="1743f-109">**TAPI 2. x:** Vedere [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span><span class="sxs-lookup"><span data-stu-id="1743f-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="1743f-110">**TAPI 3. x:** Vedere [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="1743f-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
