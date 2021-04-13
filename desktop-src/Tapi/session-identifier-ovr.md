---
description: TAPI assegna gli identificatori di sessione univoci per ogni sessione e applicazione.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificatore session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401800"
---
# <a name="session-identifier"></a><span data-ttu-id="991b1-103">Identificatore session</span><span class="sxs-lookup"><span data-stu-id="991b1-103">Session Identifier</span></span>

<span data-ttu-id="991b1-104">TAPI assegna gli identificatori di sessione univoci per ogni sessione e applicazione.</span><span class="sxs-lookup"><span data-stu-id="991b1-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="991b1-105">Un'applicazione usa un identificatore di sessione per comunicare con TAPI per una sessione specifica.</span><span class="sxs-lookup"><span data-stu-id="991b1-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="991b1-106">Un'applicazione ottiene in genere un identificatore creando una nuova sessione di comunicazione o quando TAPI offre una sessione.</span><span class="sxs-lookup"><span data-stu-id="991b1-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="991b1-107">Impossibile utilizzare un identificatore di sessione per passare informazioni a un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="991b1-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="991b1-108">A questo scopo, usare l' [ID chiamata](call-id-ovr.md), che può essere assegnato da un provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="991b1-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="991b1-109">Vedere [avviare una sessione](initiate-a-session-ovr.md) per informazioni sulle operazioni che creano sessioni e restituiscono un identificatore di sessione.</span><span class="sxs-lookup"><span data-stu-id="991b1-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="991b1-110">Vedere [rispondere a una sessione avviata altrove](respond-to-session-initiated-elsewhere-ovr.md) per le operazioni che acquisiscono gli identificatori di sessione da TAPI.</span><span class="sxs-lookup"><span data-stu-id="991b1-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="991b1-111">Per informazioni sul rilascio delle risorse della sessione, vedere [terminare una sessione](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="991b1-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="991b1-112">Tutti i provider di servizi devono supportare una forma di identificazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="991b1-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="991b1-113">**TAPI 2. x:** L'identificatore primario di una sessione di comunicazione è l'handle di chiamata.</span><span class="sxs-lookup"><span data-stu-id="991b1-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="991b1-114">**TAPI 3. x:** Una sessione è rappresentata da un [oggetto chiamata](call-object.md) e l'identificatore primario è un puntatore all'interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="991b1-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



