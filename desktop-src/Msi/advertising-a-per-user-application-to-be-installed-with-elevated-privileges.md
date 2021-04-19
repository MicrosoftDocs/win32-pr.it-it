---
description: "Per annunciare un'applicazione in base all'installazione per utente quando l'applicazione richiede privilegi elevati (ovvero di sistema) per l'installazione, usare le linee guida riportate nell'elenco seguente:"
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Annuncio di un'applicazione Per-User da installare con privilegi elevati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311065"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a><span data-ttu-id="65b48-103">Annuncio di un'applicazione Per-User da installare con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="65b48-103">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>

<span data-ttu-id="65b48-104">Per annunciare un'applicazione in base all'installazione per utente quando l'applicazione richiede privilegi elevati (ovvero di sistema) per l'installazione, usare le linee guida riportate nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="65b48-104">To advertise an application on a per-user installation basis when the application requires elevated (that is, system) privileges for installation, use the guidelines in the following list:</span></span>

-   <span data-ttu-id="65b48-105">Il processo deve essere un servizio eseguito con l'account di sistema LocalSystem in Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="65b48-105">Your process must be a service that runs under the LocalSystem system account on Windows XP or later.</span></span>
-   <span data-ttu-id="65b48-106">Generare uno script di annuncio chiamando [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) o [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span><span class="sxs-lookup"><span data-stu-id="65b48-106">Generate an advertise script by calling [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) or [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span></span>
-   <span data-ttu-id="65b48-107">Il processo deve rappresentare l'utente che è la destinazione dell'annuncio.</span><span class="sxs-lookup"><span data-stu-id="65b48-107">Your process must impersonate the user that is the target for the advertisement.</span></span>
-   <span data-ttu-id="65b48-108">Chiamare [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)e usare i \_ \| tasti di \_ \_ \| \_ \_ \| \_ scelta rapida SCRIPTFLAGS CACHEINFO SCRIPTFLAGS REGDATA appinfo SCRIPTFLAGS REGDATA CNFGINFO SCRIPTFLAGS.</span><span class="sxs-lookup"><span data-stu-id="65b48-108">Call [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta), and use the flags SCRIPTFLAGS\_CACHEINFO \| SCRIPTFLAGS\_REGDATA\_APPINFO \| SCRIPTFLAGS\_REGDATA\_CNFGINFO \| SCRIPTFLAGS\_SHORTCUTS.</span></span>

<span data-ttu-id="65b48-109">Quando si seguono le linee guida, si annuncia un'applicazione a un utente specifico e quando l'utente sceglie di installare, l'applicazione viene installata con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="65b48-109">When you follow the guidelines, you advertise an application to a specified user, and when the user chooses to install, the application is installed with elevated privileges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65b48-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65b48-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65b48-111">Applicazione di patch Per-User applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="65b48-111">Patching Per-User Managed Applications</span></span>](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



