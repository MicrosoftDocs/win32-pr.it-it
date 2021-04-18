---
title: Utente specificato
description: Utente specificato
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298000"
---
# <a name="specified-user"></a><span data-ttu-id="2773d-103">Utente specificato</span><span class="sxs-lookup"><span data-stu-id="2773d-103">Specified User</span></span>

<span data-ttu-id="2773d-104">Specificare un utente specifico (e la password dell'utente) è l'identità preferita per i server COM.</span><span class="sxs-lookup"><span data-stu-id="2773d-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="2773d-105">Il motivo per cui questa identità è preferibile è che nessuno deve essere registrato nel computer in cui è in esecuzione il server per l'esecuzione del server e ogni client comunica con la stessa istanza del server se il server ne registra la class factory come multiutilizzo.</span><span class="sxs-lookup"><span data-stu-id="2773d-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="2773d-106">Se il server dispone di un'interfaccia utente grafica, non scegliere questa identità; in tal caso, l'utente non sarà in grado di visualizzare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2773d-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="2773d-107">Questo tipo di server ha un token primario e può accedere alle risorse remote in cui un server con l'identità dell'utente che ha avviato l'avvio potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="2773d-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="2773d-108">Per ulteriori informazioni sui token di accesso e di rappresentazione, vedere [livelli di rappresentazione](impersonation-levels.md) e [mascheramento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="2773d-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="2773d-109">L'esecuzione come account utente fisso è più sicura dell'identità utente interattiva perché questa identità può essere assegnata all'applicazione solo da un utente che ha la password di un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="2773d-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2773d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2773d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2773d-111">Identità applicazione</span><span class="sxs-lookup"><span data-stu-id="2773d-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="2773d-112">Utente interattivo</span><span class="sxs-lookup"><span data-stu-id="2773d-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="2773d-113">Avvio dell'utente</span><span class="sxs-lookup"><span data-stu-id="2773d-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="2773d-114">Identità del servizio</span><span class="sxs-lookup"><span data-stu-id="2773d-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




