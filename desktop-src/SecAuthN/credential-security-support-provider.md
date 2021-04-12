---
description: Credential Security Support Provider Protocol (CredSSP) è un provider di supporto per la sicurezza implementato mediante SSPI (Security Support Provider Interface).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Provider di supporto per la sicurezza delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226485"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="8acde-103">Provider di supporto per la sicurezza delle credenziali</span><span class="sxs-lookup"><span data-stu-id="8acde-103">Credential Security Support Provider</span></span>

<span data-ttu-id="8acde-104">Credential Security Support Provider Protocol (CredSSP) è un provider di supporto per la sicurezza implementato mediante[SSPI](sspi.md)(Security Support Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="8acde-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="8acde-105">CredSSP consente a un'applicazione di delegare le credenziali dell'utente dal client al server di destinazione per l'autenticazione remota.</span><span class="sxs-lookup"><span data-stu-id="8acde-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="8acde-106">CredSSP fornisce un canale di [protocollo Transport Layer Security](transport-layer-security-protocol.md) crittografato.</span><span class="sxs-lookup"><span data-stu-id="8acde-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="8acde-107">Il client viene autenticato sul canale crittografato utilizzando il protocollo Negotiate (Simple and protected Negotiate, SPNEGO) con [Microsoft Kerberos](microsoft-kerberos.md) o [Microsoft NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="8acde-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="8acde-108">La delega non è vincolata.</span><span class="sxs-lookup"><span data-stu-id="8acde-108">This is not constrained delegation.</span></span> <span data-ttu-id="8acde-109">CredSSP passa le credenziali complete dell'utente al server senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="8acde-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="8acde-110">Per informazioni su SPNEGO, vedere [Microsoft Negotiate](microsoft-negotiate.md).</span><span class="sxs-lookup"><span data-stu-id="8acde-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="8acde-111">Dopo l'autenticazione del client e del server, il client passa le credenziali dell'utente al server.</span><span class="sxs-lookup"><span data-stu-id="8acde-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="8acde-112">Le credenziali vengono crittografate doppiamente nelle chiavi di sessione SPNEGO e TLS.</span><span class="sxs-lookup"><span data-stu-id="8acde-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="8acde-113">CredSSP supporta l'accesso basato su password, nonché l'accesso tramite smart card basato su [*X. 509*](/windows/desktop/SecGloss/x-gly) e PKINIT.</span><span class="sxs-lookup"><span data-stu-id="8acde-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8acde-114">CredSSP non supporta client WOW64.</span><span class="sxs-lookup"><span data-stu-id="8acde-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="8acde-115">Per ulteriori informazioni su CredSSP, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="8acde-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="8acde-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="8acde-116">Topic</span></span>                                                                         | <span data-ttu-id="8acde-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8acde-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8acde-118">Impostazioni Criteri di gruppo CredSSP</span><span class="sxs-lookup"><span data-stu-id="8acde-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="8acde-119">La delega delle credenziali da CredSSP può essere controllata tramite le impostazioni di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8acde-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

