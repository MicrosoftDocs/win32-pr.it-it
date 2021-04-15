---
title: Creazione di finestre e desktop
description: Il sistema crea automaticamente la stazione finestra interattiva.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337486"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="32352-103">Creazione di finestre e desktop</span><span class="sxs-lookup"><span data-stu-id="32352-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="32352-104">Il sistema crea automaticamente la stazione finestra interattiva.</span><span class="sxs-lookup"><span data-stu-id="32352-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="32352-105">Quando un utente interattivo esegue l'accesso, il sistema associa la stazione interattiva della finestra alla sessione di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="32352-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="32352-106">Il sistema crea anche il desktop di input predefinito per la stazione finestra interattiva ( \\ impostazione predefinita WinSta0).</span><span class="sxs-lookup"><span data-stu-id="32352-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="32352-107">I processi avviati dall'utente connesso sono associati al \\ desktop predefinito di WinSta0.</span><span class="sxs-lookup"><span data-stu-id="32352-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="32352-108">Un processo può utilizzare la funzione [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) per creare una nuova stazione di finestra e la funzione **CreateDesktop** o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) per creare un nuovo desktop.</span><span class="sxs-lookup"><span data-stu-id="32352-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="32352-109">Il numero di desktop che è possibile creare è limitato dalle dimensioni dell'heap del desktop di sistema.</span><span class="sxs-lookup"><span data-stu-id="32352-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="32352-110">Per ulteriori informazioni, vedere [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="32352-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="32352-111">Quando un processo non interattivo, ad esempio un'applicazione di servizio, tenta di connettersi a una stazione di Windows e non esiste alcuna stazione di finestra per la sessione di accesso al processo, il sistema tenta di creare una stazione di finestra e un desktop per la sessione.</span><span class="sxs-lookup"><span data-stu-id="32352-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="32352-112">Il nome della stazione di finestra creata è basato sull'identificatore della sessione di accesso e il desktop è denominato predefinito, come descritto di seguito:</span><span class="sxs-lookup"><span data-stu-id="32352-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="32352-113">Se un servizio è in esecuzione nel contesto di sicurezza dell'account LocalSystem ma non include l'attributo SERVICE \_ Interactive \_ Process, usa la finestra di Windows Station e desktop: Service-0x0-3e7 $ \\ default.</span><span class="sxs-lookup"><span data-stu-id="32352-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="32352-114">Questa finestra non è interattiva, quindi il servizio non è in grado di visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="32352-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="32352-115">Inoltre, i processi creati dal servizio non possono visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="32352-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="32352-116">Se il servizio è in esecuzione nel contesto di sicurezza di un account utente, il nome della stazione della finestra è basato sul servizio SID utente-0x *Z1* - *Z2*$, dove *Z1* è la parte superiore del SID di accesso e *Z2* è la parte inferiore del SID di accesso.</span><span class="sxs-lookup"><span data-stu-id="32352-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="32352-117">Poiché un SID è univoco per la sessione di accesso, due servizi in esecuzione nello stesso contesto di sicurezza ricevono stazioni della finestra univoche.</span><span class="sxs-lookup"><span data-stu-id="32352-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="32352-118">Queste stazioni della finestra non sono interattive.</span><span class="sxs-lookup"><span data-stu-id="32352-118">These window stations are not interactive.</span></span>

<span data-ttu-id="32352-119">L'elenco di controllo di accesso discrezionale (DACL) per la finestra stazione e il desktop include i seguenti diritti di accesso per l'account utente del servizio:</span><span class="sxs-lookup"><span data-stu-id="32352-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="32352-120">Stazione finestra:</span><span class="sxs-lookup"><span data-stu-id="32352-120">Window Station:</span></span>

<dl> <span data-ttu-id="32352-121">\_ACCESSCLIPBOARD winsta</span><span class="sxs-lookup"><span data-stu-id="32352-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="32352-122">\_ACCESSGLOBALATOMS winsta</span><span class="sxs-lookup"><span data-stu-id="32352-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="32352-123">\_CREATEDESKTOP winsta</span><span class="sxs-lookup"><span data-stu-id="32352-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="32352-124">\_EXITWINDOWS winsta</span><span class="sxs-lookup"><span data-stu-id="32352-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="32352-125">\_diritti READATTRIBUTES winsta</span><span class="sxs-lookup"><span data-stu-id="32352-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="32352-126">\_diritti standard \_ richiesti</span><span class="sxs-lookup"><span data-stu-id="32352-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="32352-127">Desktop:</span><span class="sxs-lookup"><span data-stu-id="32352-127">Desktop:</span></span>

<dl> <span data-ttu-id="32352-128">\_CREATEMENU desktop</span><span class="sxs-lookup"><span data-stu-id="32352-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="32352-129">\_CREATEWINDOW desktop</span><span class="sxs-lookup"><span data-stu-id="32352-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="32352-130">\_enumerazione desktop</span><span class="sxs-lookup"><span data-stu-id="32352-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="32352-131">\_HOOKCONTROL desktop</span><span class="sxs-lookup"><span data-stu-id="32352-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="32352-132">\_READOBJECTS desktop</span><span class="sxs-lookup"><span data-stu-id="32352-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="32352-133">\_WRITEOBJECTS desktop</span><span class="sxs-lookup"><span data-stu-id="32352-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="32352-134">\_diritti standard \_ richiesti</span><span class="sxs-lookup"><span data-stu-id="32352-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 