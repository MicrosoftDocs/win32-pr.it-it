---
description: L'oggetto Request viene creato utilizzando COM CoCreateInstance ed espone un'interfaccia, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Oggetto Request
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311878"
---
# <a name="request-object"></a><span data-ttu-id="93941-103">Oggetto Request</span><span class="sxs-lookup"><span data-stu-id="93941-103">Request Object</span></span>

<span data-ttu-id="93941-104">L'oggetto Request viene creato utilizzando COM **CoCreateInstance** ed espone un'interfaccia, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span><span class="sxs-lookup"><span data-stu-id="93941-104">The Request Object is created using COM **CoCreateInstance** and exposes one interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span></span> <span data-ttu-id="93941-105">Questa interfaccia espone il metodo [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , che consente a un'applicazione TAPI 3 di utilizzare la telefonia assistita.</span><span class="sxs-lookup"><span data-stu-id="93941-105">This interface exposes the [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) method, which allows a TAPI 3 application to use Assisted Telephony.</span></span> <span data-ttu-id="93941-106">La telefonia assistita offre applicazioni abilitate per la telefonia con un semplice meccanismo per effettuare chiamate telefoniche senza che lo sviluppatore debba essere completamente alfabetizzato nella telefonia.</span><span class="sxs-lookup"><span data-stu-id="93941-106">Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.</span></span>

<span data-ttu-id="93941-107">Ad esempio, un'applicazione per fogli di calcolo può aggiungere un pulsante "make Call" utilizzando la telefonia assistita senza implementare i controlli più elaborati disponibili in un'applicazione TAPI completa.</span><span class="sxs-lookup"><span data-stu-id="93941-107">For example, a spreadsheet application can add a "Make Call" button using Assisted Telephony without implementing the more elaborate controls available in a full TAPI application.</span></span>

<span data-ttu-id="93941-108">Per ulteriori informazioni, vedere la [Panoramica della telefonia assistita](assisted-telephony-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="93941-108">See the [Assisted Telephony Overview](assisted-telephony-overview.md) for additional information.</span></span>

 

 



