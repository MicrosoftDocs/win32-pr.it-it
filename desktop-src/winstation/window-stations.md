---
title: Stazioni finestra
description: Una finestra di Windows contiene gli appunti, una tabella Atom e uno o più oggetti desktop. Ogni oggetto della stazione di finestra è un oggetto a protezione diretta. Quando viene creata, una stazione di finestra viene associata al processo chiamante e assegnata alla sessione corrente.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- oggetti Window Station
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046916"
---
# <a name="window-stations"></a><span data-ttu-id="64927-106">Stazioni finestra</span><span class="sxs-lookup"><span data-stu-id="64927-106">Window Stations</span></span>

<span data-ttu-id="64927-107">Una *finestra di Windows* contiene gli appunti, una tabella Atom e uno o più oggetti [Desktop](desktops.md) .</span><span class="sxs-lookup"><span data-stu-id="64927-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="64927-108">Ogni oggetto della stazione di finestra è un oggetto a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="64927-108">Each window station object is a securable object.</span></span> <span data-ttu-id="64927-109">Quando viene creata, una stazione di finestra viene associata al processo chiamante e assegnata alla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="64927-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="64927-110">*Interactive Window Station* è l'unica finestra che può visualizzare un'interfaccia utente o ricevere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64927-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="64927-111">Viene assegnato alla sessione di accesso dell'utente interattivo e contiene la tastiera, il mouse e il dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="64927-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="64927-112">Viene sempre denominato "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="64927-112">It is always named "WinSta0".</span></span> <span data-ttu-id="64927-113">Tutte le altre stazioni della finestra sono non interattive, il che significa che non possono visualizzare un'interfaccia utente o ricevere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64927-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="64927-114">Quando un utente accede a un computer utilizzando Servizi Desktop remoto, viene avviata una sessione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="64927-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="64927-115">Ogni sessione è associata alla propria finestra interattiva denominata "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="64927-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="64927-116">Per ulteriori informazioni, vedere [Desktop remoto Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span><span class="sxs-lookup"><span data-stu-id="64927-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="64927-117">Per ulteriori informazioni sulle stazioni della finestra, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="64927-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="64927-118">Creazione di finestre e desktop</span><span class="sxs-lookup"><span data-stu-id="64927-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="64927-119">Elaborare la connessione a una stazione di finestra</span><span class="sxs-lookup"><span data-stu-id="64927-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="64927-120">Diritti di accesso e sicurezza di Windows Station</span><span class="sxs-lookup"><span data-stu-id="64927-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 