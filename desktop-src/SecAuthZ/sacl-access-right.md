---
description: Il \_ \_ diritto di accesso di sicurezza del sistema Access controlla la possibilità di ottenere o impostare l'elenco SACL in un descrittore di sicurezza degli oggetti. Il sistema concede questo diritto di accesso se il \_ \_ privilegio per il nome di sicurezza se è abilitato nel token di accesso del thread richiedente.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Accesso SACL a destra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308138"
---
# <a name="sacl-access-right"></a><span data-ttu-id="93c04-104">Accesso SACL a destra</span><span class="sxs-lookup"><span data-stu-id="93c04-104">SACL Access Right</span></span>

<span data-ttu-id="93c04-105">Il \_ \_ diritto di accesso di sicurezza del sistema Access controlla la possibilità di ottenere o impostare l'elenco SACL nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="93c04-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="93c04-106">Il sistema concede questo diritto di accesso solo se il \_ \_ privilegio del nome di sicurezza se è abilitato nel [*token di accesso*](/windows/desktop/SecGloss/a-gly) del thread richiedente.</span><span class="sxs-lookup"><span data-stu-id="93c04-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="93c04-107">**Per accedere al SACL di un oggetto**</span><span class="sxs-lookup"><span data-stu-id="93c04-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="93c04-108">Chiamare la funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare il \_ privilegio se \_ nome di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93c04-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="93c04-109">\_ \_ Quando si apre un handle per l'oggetto, richiedere il diritto di accesso di sicurezza del sistema di accesso.</span><span class="sxs-lookup"><span data-stu-id="93c04-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="93c04-110">Ottenere o impostare il SACL dell'oggetto utilizzando una funzione quale [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span><span class="sxs-lookup"><span data-stu-id="93c04-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="93c04-111">Chiamare [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per disabilitare il privilegio se il \_ nome di sicurezza \_ .</span><span class="sxs-lookup"><span data-stu-id="93c04-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="93c04-112">Per accedere a un SACL usando le funzioni [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , abilitare il \_ \_ privilegio se nome sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93c04-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="93c04-113">La funzione richiede internamente il diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="93c04-113">The function internally requests the access right.</span></span>

<span data-ttu-id="93c04-114">Il \_ diritto di \_ accesso di sicurezza del sistema di accesso non è valido in un DACL perché gli elenchi DACL non controllano l'accesso a un SACL.</span><span class="sxs-lookup"><span data-stu-id="93c04-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="93c04-115">Tuttavia, è possibile usare il \_ diritto di accesso di sicurezza del sistema di accesso \_ in un SACL per controllare i tentativi di usare il diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="93c04-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
