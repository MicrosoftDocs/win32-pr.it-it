---
description: Elenca le esportazioni di DLL che devono essere implementate per creare una gestione credenziali.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementazione di gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884506"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="9e701-103">Implementazione di gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="9e701-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="9e701-104">Per creare una gestione credenziali, è necessario creare una DLL che esporti le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e701-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="9e701-105">**NPLogonNotify**</span><span class="sxs-lookup"><span data-stu-id="9e701-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="9e701-106">**NPPasswordChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="9e701-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="9e701-107">Per ripristinare le notifiche per le funzioni [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) per l'accesso con smart card, creare una voce del registro di sistema denominata **SmartCardLogonNotify** come **DWORD** e impostarla su 1:</span><span class="sxs-lookup"><span data-stu-id="9e701-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="9e701-108">**Windows Server 2003 e Windows XP:** La voce del registro di sistema **SmartCardLogonNotify** non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="9e701-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="9e701-109">Inoltre, i gestori delle credenziali devono supportare anche la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) per l'avvio di WNNC \_ (il supporto di altri indici non è necessario per i gestori delle credenziali).</span><span class="sxs-lookup"><span data-stu-id="9e701-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="9e701-110">Ciò indica a MPR quando viene avviato un gestore delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9e701-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="9e701-111">Chiamando **NPGetCaps** con il parametro *NINDEX* impostato su WNNC \_ Start, il MPR ottiene il tempo di attesa prima di chiamare le funzioni del punto di ingresso di gestione delle credenziali del provider.</span><span class="sxs-lookup"><span data-stu-id="9e701-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="9e701-112">Se il server di gestione delle credenziali dispone di queste informazioni, è possibile inviarlo a gestione credenziali, impostando il timeout.</span><span class="sxs-lookup"><span data-stu-id="9e701-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 



