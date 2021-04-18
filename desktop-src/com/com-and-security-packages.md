---
title: Pacchetti COM e di sicurezza
description: Windows supporta NTLMSSP (LAN Manager Security Support Provider), il protocollo di autenticazione Kerberos V5 e il pacchetto di sicurezza Schannel, che fornisce i protocolli PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297975"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="4ab2f-103">Pacchetti COM e di sicurezza</span><span class="sxs-lookup"><span data-stu-id="4ab2f-103">COM and Security Packages</span></span>

<span data-ttu-id="4ab2f-104">Windows supporta NTLMSSP (LAN Manager Security Support Provider), il protocollo di autenticazione Kerberos V5 e il pacchetto di sicurezza Schannel, che fornisce i protocolli PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="4ab2f-105">È supportato anche Snego, che verifica la disponibilità dei pacchetti di sicurezza e seleziona quello più appropriato.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="4ab2f-106">La tabella seguente illustra i livelli di autenticazione supportati dai diversi pacchetti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="4ab2f-107">Autenticazione server/client</span><span class="sxs-lookup"><span data-stu-id="4ab2f-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="4ab2f-108">Supporto del pacchetto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="4ab2f-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="4ab2f-109">Nessuno dei due può ottenere il nome dell'altro.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="4ab2f-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="4ab2f-110">None</span></span><br/>                                                  |
| <span data-ttu-id="4ab2f-111">Il client può autenticare il server, ma non viceversa.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="4ab2f-112">SChannel</span><span class="sxs-lookup"><span data-stu-id="4ab2f-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="4ab2f-113">Il client non è in grado di individuare il server, ma il server può ottenere l'ID utente del client.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="4ab2f-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="4ab2f-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="4ab2f-115">Autenticazione reciproca: il client e il server possono conoscerne il nome, se l'autorizzazione è concessa.</span><span class="sxs-lookup"><span data-stu-id="4ab2f-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="4ab2f-116">NTLMSSP (in locale), protocollo Kerberos V5 e Schannel</span><span class="sxs-lookup"><span data-stu-id="4ab2f-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="4ab2f-117">Per ulteriori informazioni su questi pacchetti di sicurezza, vedere gli argomenti seguenti in questa sezione:</span><span class="sxs-lookup"><span data-stu-id="4ab2f-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="4ab2f-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="4ab2f-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="4ab2f-119">Protocollo Kerberos V5</span><span class="sxs-lookup"><span data-stu-id="4ab2f-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="4ab2f-120">Schannel</span><span class="sxs-lookup"><span data-stu-id="4ab2f-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="4ab2f-121">Snego</span><span class="sxs-lookup"><span data-stu-id="4ab2f-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="4ab2f-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ab2f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ab2f-123">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="4ab2f-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





