---
description: L'account LocalService è un account locale predefinito utilizzato da Gestione controllo servizi.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Account LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529868"
---
# <a name="localservice-account"></a><span data-ttu-id="77ae4-103">Account LocalService</span><span class="sxs-lookup"><span data-stu-id="77ae4-103">LocalService Account</span></span>

<span data-ttu-id="77ae4-104">L'account LocalService è un account locale predefinito utilizzato da Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="77ae4-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="77ae4-105">Dispone dei privilegi minimi nel computer locale e presenta credenziali anonime sulla rete.</span><span class="sxs-lookup"><span data-stu-id="77ae4-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="77ae4-106">Questo account può essere specificato in una chiamata alle funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="77ae4-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="77ae4-107">Si noti che questo account non dispone di una password, pertanto tutte le informazioni sulla password fornite in questa chiamata verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="77ae4-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="77ae4-108">Mentre il sottosistema di sicurezza localizza il nome dell'account, SCM non supporta i nomi localizzati.</span><span class="sxs-lookup"><span data-stu-id="77ae4-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="77ae4-109">Si riceverà pertanto un nome localizzato per questo account dalla funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , ma il nome dell'account deve essere NT Authority \\ LocalService quando si chiama **CreateService** o **ChangeServiceConfig**, indipendentemente dalle impostazioni locali, oppure possono verificarsi risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="77ae4-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="77ae4-110">Il SID utente viene creato dal valore **\_ \_ \_ RID servizio locale di sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="77ae4-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="77ae4-111">L'account LocalService ha una propria sottochiave nella chiave del registro di sistema **\_ utenti di HKEY** .</span><span class="sxs-lookup"><span data-stu-id="77ae4-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="77ae4-112">La chiave del registro di sistema dell' **\_ \_ utente corrente di HKEY** è quindi associata all'account LocalService.</span><span class="sxs-lookup"><span data-stu-id="77ae4-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="77ae4-113">L'account LocalService presenta i privilegi seguenti:</span><span class="sxs-lookup"><span data-stu-id="77ae4-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="77ae4-114">**Se \_ \_Nome ASSIGNPRIMARYTOKEN** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="77ae4-115">**Se \_ \_Nome controllo** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="77ae4-116">**Se \_ MODIFICA \_ \_ nome notifica** (abilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="77ae4-117">**Se \_ Crea \_ \_ nome globale** (abilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="77ae4-118">**Se \_ \_Nome rappresentazione** (abilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="77ae4-119">**Se \_ AUMENTA \_ il \_ nome della quota** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="77ae4-120">**Se \_ \_Nome arresto** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="77ae4-121">**Se \_ Annulla ancoraggio \_ nome** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="77ae4-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="77ae4-122">Tutti i privilegi assegnati agli utenti e agli utenti autenticati</span><span class="sxs-lookup"><span data-stu-id="77ae4-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="77ae4-123">Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="77ae4-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
