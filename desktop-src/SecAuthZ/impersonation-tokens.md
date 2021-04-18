---
description: Viene illustrato l'utilizzo dei token di rappresentazione nel controllo di accesso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Token di rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317046"
---
# <a name="impersonation-tokens"></a><span data-ttu-id="d6a45-103">Token di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="d6a45-103">Impersonation Tokens</span></span>

<span data-ttu-id="d6a45-104">Un thread di rappresentazione ha due [*token di accesso*](/windows/desktop/SecGloss/a-gly):</span><span class="sxs-lookup"><span data-stu-id="d6a45-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="d6a45-105">Un [*token di accesso primario*](/windows/desktop/SecGloss/p-gly) che descrive il [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) del server.</span><span class="sxs-lookup"><span data-stu-id="d6a45-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="d6a45-106">Per ottenere un handle per questo token, chiamare la funzione [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .</span><span class="sxs-lookup"><span data-stu-id="d6a45-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="d6a45-107">Un token di accesso di rappresentazione che descrive il contesto di sicurezza del client rappresentato.</span><span class="sxs-lookup"><span data-stu-id="d6a45-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="d6a45-108">Per ottenere un handle per questo token, chiamare la funzione [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .</span><span class="sxs-lookup"><span data-stu-id="d6a45-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="d6a45-109">Un server può utilizzare il [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly) nelle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6a45-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="d6a45-110">Nelle funzioni [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)e [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per determinare se un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) consente al client un set di diritti di accesso.</span><span class="sxs-lookup"><span data-stu-id="d6a45-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="d6a45-111">Nella funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare o disabilitare i privilegi del client.</span><span class="sxs-lookup"><span data-stu-id="d6a45-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="d6a45-112">Nella funzione [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare se un set di privilegi è abilitato nel token del client.</span><span class="sxs-lookup"><span data-stu-id="d6a45-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="d6a45-113">In funzioni che generano voci nel registro eventi di sicurezza, ad esempio [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) o [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span><span class="sxs-lookup"><span data-stu-id="d6a45-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="d6a45-114">Queste funzioni usano un token di rappresentazione per ottenere informazioni sul client per la voce di log.</span><span class="sxs-lookup"><span data-stu-id="d6a45-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
