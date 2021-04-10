---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modalità protetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882610"
---
# <a name="protected-mode"></a><span data-ttu-id="07d57-103">Modalità protetta</span><span class="sxs-lookup"><span data-stu-id="07d57-103">Protected Mode</span></span>

<span data-ttu-id="07d57-104">La maggior parte delle funzionalità di sicurezza di Windows Internet Explorer 8 sono disponibili in Internet Explorer 8 per il sistema operativo Windows XP con Service Pack 2 (SP2) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="07d57-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="07d57-105">La modalità protetta è disponibile solo per Windows Vista o versioni successive perché si basa sulle seguenti funzionalità di sicurezza nuove per Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="07d57-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="07d57-106">Il [controllo dell'account utente](https://msdn.microsoft.com/library/aa511445.aspx) facilita l'esecuzione senza privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="07d57-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="07d57-107">Quando gli utenti eseguono programmi con privilegi utente limitati, è più sicuro da un attacco rispetto a quando vengono eseguiti con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="07d57-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="07d57-108">Il sistema operativo Windows può limitare l'esecuzione di azioni dannose da parte del codice dannoso.</span><span class="sxs-lookup"><span data-stu-id="07d57-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="07d57-109">Un meccanismo di integrità limita l'accesso in scrittura agli [oggetti a protezione diretta](../secauthz/securable-objects.md) mediante processi di integrità inferiore, nello stesso modo in cui l'appartenenza a un gruppo di account utente limita i diritti di accesso degli utenti ai componenti di sistema sensibili.</span><span class="sxs-lookup"><span data-stu-id="07d57-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="07d57-110">L' [isolamento dei privilegi dell'interfaccia utente (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impedisce ai processi di inviare messaggi della finestra selezionati e altre API utente ai processi in esecuzione con maggiore integrità.</span><span class="sxs-lookup"><span data-stu-id="07d57-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="07d57-111">L'infrastruttura di sicurezza di Windows Integrity Mechanism consente la modalità protetta per fornire a Windows Internet Explorer i privilegi necessari agli utenti per esplorare il Web, negando al tempo stesso i privilegi necessari agli utenti per l'installazione automatica dei programmi o la modifica dei dati di sistema sensibili.</span><span class="sxs-lookup"><span data-stu-id="07d57-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="07d57-112">Gli utenti possono disabilitare questa funzionalità tramite una casella di controllo e gli amministratori possono disabilitarla utilizzando Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="07d57-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07d57-113">È necessario disabilitare la funzionalità solo come misura temporanea durante la risoluzione dei problemi per confrontare il comportamento dell'applicazione quando la funzionalità è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="07d57-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="07d57-114">Si consiglia di lasciare la funzionalità abilitata in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="07d57-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="07d57-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07d57-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d57-116">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="07d57-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
