---
description: L'account NetworkService è un account locale predefinito utilizzato da Gestione controllo servizi.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Account NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316614"
---
# <a name="networkservice-account"></a><span data-ttu-id="59cf4-103">Account NetworkService</span><span class="sxs-lookup"><span data-stu-id="59cf4-103">NetworkService Account</span></span>

<span data-ttu-id="59cf4-104">L'account NetworkService è un account locale predefinito utilizzato da Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="59cf4-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="59cf4-105">Questo account non è riconosciuto dal sottosistema di sicurezza, pertanto non è possibile specificarne il nome in una chiamata alla funzione [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .</span><span class="sxs-lookup"><span data-stu-id="59cf4-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="59cf4-106">Dispone dei privilegi minimi nel computer locale e funge da computer in rete.</span><span class="sxs-lookup"><span data-stu-id="59cf4-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="59cf4-107">Questo account può essere specificato in una chiamata alle funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="59cf4-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="59cf4-108">Si noti che questo account non dispone di una password, pertanto tutte le informazioni sulla password fornite in questa chiamata verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="59cf4-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="59cf4-109">Mentre il sottosistema di sicurezza localizza il nome dell'account, SCM non supporta i nomi localizzati.</span><span class="sxs-lookup"><span data-stu-id="59cf4-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="59cf4-110">Si riceverà pertanto un nome localizzato per questo account dalla funzione [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , ma il nome dell'account deve essere NT Authority \\ NetworkService quando si chiama **CreateService** o **ChangeServiceConfig**, indipendentemente dalle impostazioni locali, oppure possono verificarsi risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="59cf4-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="59cf4-111">Un servizio eseguito nel contesto dell'account NetworkService presenta le credenziali del computer ai server remoti.</span><span class="sxs-lookup"><span data-stu-id="59cf4-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="59cf4-112">Per impostazione predefinita, il token remoto contiene i SID per i gruppi Everyone e Authenticated Users.</span><span class="sxs-lookup"><span data-stu-id="59cf4-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="59cf4-113">Il SID utente viene creato dal valore **\_ \_ \_ RID servizio di rete di sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="59cf4-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="59cf4-114">L'account NetworkService ha una propria sottochiave sotto la chiave del registro di sistema **HKEY \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="59cf4-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="59cf4-115">La chiave del registro di sistema dell' **\_ \_ utente corrente di HKEY** è quindi associata all'account NetworkService.</span><span class="sxs-lookup"><span data-stu-id="59cf4-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="59cf4-116">L'account NetworkService dispone dei privilegi seguenti:</span><span class="sxs-lookup"><span data-stu-id="59cf4-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="59cf4-117">**Se \_ \_Nome ASSIGNPRIMARYTOKEN** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="59cf4-118">**Se \_ \_Nome controllo** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="59cf4-119">**Se \_ MODIFICA \_ \_ nome notifica** (abilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="59cf4-120">**Se \_ Crea \_ \_ nome globale** (abilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="59cf4-121">**Se \_ \_Nome rappresentazione** (abilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="59cf4-122">**Se \_ AUMENTA \_ il \_ nome della quota** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="59cf4-123">**Se \_ \_Nome arresto** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="59cf4-124">**Se \_ Annulla ancoraggio \_ nome** (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="59cf4-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="59cf4-125">Tutti i privilegi assegnati agli utenti e agli utenti autenticati</span><span class="sxs-lookup"><span data-stu-id="59cf4-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="59cf4-126">Per ulteriori informazioni, vedere [sicurezza del servizio e diritti di accesso](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="59cf4-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
