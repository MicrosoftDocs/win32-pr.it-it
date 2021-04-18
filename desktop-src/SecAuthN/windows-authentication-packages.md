---
description: I pacchetti di autenticazione di Windows forniscono servizi di autenticazione implementando funzionalità specifiche del pacchetto per le funzioni LsaLogonUser e LsaCallAuthenticationPackage fornite da LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Pacchetti di autenticazione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525843"
---
# <a name="windows-authentication-packages"></a><span data-ttu-id="61acb-103">Pacchetti di autenticazione di Windows</span><span class="sxs-lookup"><span data-stu-id="61acb-103">Windows Authentication Packages</span></span>

<span data-ttu-id="61acb-104">I pacchetti di autenticazione di Windows forniscono servizi di autenticazione implementando funzionalità specifiche del pacchetto per le funzioni [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) e [**LSACALLAUTHENTICATIONPACKAGE**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fornite da LSA.</span><span class="sxs-lookup"><span data-stu-id="61acb-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="61acb-105">MSV1 \_ 0 è un esempio di pacchetto di [*autenticazione*](../secgloss/a-gly.md)di Windows.</span><span class="sxs-lookup"><span data-stu-id="61acb-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="61acb-106">Il \_ pacchetto MSV1 0 accetta un nome utente e una password con [*hash*](../secgloss/h-gly.md) , che cerca nel database [*Gestione account di sicurezza*](../secgloss/s-gly.md) (Sam).</span><span class="sxs-lookup"><span data-stu-id="61acb-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="61acb-107">A seconda dei risultati della ricerca, il \_ pacchetto di autenticazione MSV1 0 accetta o rifiuta il tentativo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="61acb-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="61acb-108">Per un elenco delle funzioni di supporto che LSA fornisce per l'uso da parte dei pacchetti di autenticazione di Windows che richiedono i servizi di sistema, vedere [funzioni LSA chiamate dai pacchetti di autenticazione](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="61acb-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="61acb-109">I pacchetti di autenticazione di Windows devono implementare un set di funzioni chiamate da LSA.</span><span class="sxs-lookup"><span data-stu-id="61acb-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="61acb-110">Per l'elenco completo delle funzioni, vedere [funzioni implementate dai pacchetti di autenticazione](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="61acb-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
