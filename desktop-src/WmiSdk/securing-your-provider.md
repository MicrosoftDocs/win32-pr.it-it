---
description: Per la scrittura di un provider sicuro è necessario considerare la modalità di hosting del provider, il modo in cui il provider gestisce la rappresentazione e verificare che gli utenti vengano controllati per i diritti di accesso ai dati.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Sicurezza del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309884"
---
# <a name="securing-your-provider"></a><span data-ttu-id="793bc-103">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="793bc-103">Securing Your Provider</span></span>

<span data-ttu-id="793bc-104">Per la scrittura di un provider sicuro è necessario considerare la modalità di hosting del provider, il modo in cui il provider gestisce la rappresentazione e verificare che gli utenti vengano controllati per i diritti di accesso ai dati.</span><span class="sxs-lookup"><span data-stu-id="793bc-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="793bc-105">È possibile proteggere i dati nello spazio dei nomi del provider richiedendo che i dati vengano crittografati prima di inviarli in una rete.</span><span class="sxs-lookup"><span data-stu-id="793bc-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="793bc-106">Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="793bc-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="793bc-107">Se un utente dispone di accesso in **\_ scrittura completo** in qualsiasi spazio dei nomi, l'utente può creare sottoscrizioni tra gli spazi dei nomi per i dati in uno spazio dei nomi in cui l'utente è limitato.</span><span class="sxs-lookup"><span data-stu-id="793bc-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="793bc-108">Poiché un provider può essere caricato in qualsiasi spazio dei nomi ed eseguito in qualsiasi contesto di sicurezza, il provider deve eseguire i propri controlli di accesso per garantire che solo gli utenti autorizzati possano accedere ai dati o eseguire metodi.</span><span class="sxs-lookup"><span data-stu-id="793bc-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="793bc-109">Per ulteriori informazioni, vedere [esecuzione dei controlli di accesso](performing-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="793bc-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="793bc-110">Negli argomenti seguenti viene illustrata la sicurezza del provider:</span><span class="sxs-lookup"><span data-stu-id="793bc-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="793bc-111">Hosting e sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="793bc-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="793bc-112">Esecuzione di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="793bc-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="793bc-113">Chiavi del registro di sistema per il controllo della sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="793bc-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="793bc-114">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="793bc-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="793bc-115">Rappresentazione di un client</span><span class="sxs-lookup"><span data-stu-id="793bc-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="793bc-116">Negli argomenti seguenti viene illustrato come i client e gli script interagiscono con la sicurezza del provider:</span><span class="sxs-lookup"><span data-stu-id="793bc-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="793bc-117">Impostazione dell'autenticazione in WMI</span><span class="sxs-lookup"><span data-stu-id="793bc-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="793bc-118">Connessione tra sistemi operativi diversi</span><span class="sxs-lookup"><span data-stu-id="793bc-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="793bc-119">Impostazione del livello di sicurezza del processo predefinito tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="793bc-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="793bc-120">Impostazione della sicurezza del processo dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="793bc-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="793bc-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="793bc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="793bc-122">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="793bc-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="793bc-123">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="793bc-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
