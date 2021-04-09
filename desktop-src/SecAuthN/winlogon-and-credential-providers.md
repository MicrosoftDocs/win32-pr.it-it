---
description: È il modulo Windows che esegue l'accesso interattivo per una sessione di accesso. Il comportamento di Winlogon può essere personalizzato implementando e registrando un provider di credenziali.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Provider di credenziali e Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966621"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="98491-104">Provider di credenziali e Winlogon</span><span class="sxs-lookup"><span data-stu-id="98491-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="98491-105">[*Winlogon*](../secgloss/w-gly.md) è il modulo Windows che esegue l'accesso interattivo per una [*sessione di accesso*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="98491-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="98491-106">Il comportamento di Winlogon può essere personalizzato implementando e registrando un provider di credenziali.</span><span class="sxs-lookup"><span data-stu-id="98491-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="98491-107">Per informazioni sull'implementazione di un provider di credenziali, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="98491-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="98491-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="98491-108">Topic</span></span>                                                                                                           | <span data-ttu-id="98491-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98491-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98491-110">Esperienza di accesso di Windows basata su provider di credenziali</span><span class="sxs-lookup"><span data-stu-id="98491-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="98491-111">Panoramica dell'architettura di Winlogon e del provider di credenziali e di un provider di credenziali di esempio.</span><span class="sxs-lookup"><span data-stu-id="98491-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="98491-112">Interfacce della shell</span><span class="sxs-lookup"><span data-stu-id="98491-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="98491-113">Riferimento all'interfaccia del provider di credenziali.</span><span class="sxs-lookup"><span data-stu-id="98491-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="98491-114">Provider di credenziali in Windows 10</span><span class="sxs-lookup"><span data-stu-id="98491-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="98491-115">Provider di credenziali di terze parti e provider di credenziali di sistema in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="98491-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="98491-116">Per un'implementazione del provider di credenziali di esempio, vedere l'esempio che si trova nella directory di installazione di Windows SDK in \\ esempi di \\ sicurezza \\ CredentialProvider.</span><span class="sxs-lookup"><span data-stu-id="98491-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="98491-117">**Windows Server 2003 e Windows XP:** I provider di credenziali non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="98491-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="98491-118">Per informazioni sulla personalizzazione di Winlogon, vedere [Winlogon e Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="98491-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
