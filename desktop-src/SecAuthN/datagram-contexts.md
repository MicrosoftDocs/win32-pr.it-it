---
description: La semantica per i contesti di datagramma o senza connessione è leggermente diversa da quella per i contesti orientati alla connessione.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contesti di datagramma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129927"
---
# <a name="datagram-contexts"></a><span data-ttu-id="a382d-103">Contesti di datagramma</span><span class="sxs-lookup"><span data-stu-id="a382d-103">Datagram Contexts</span></span>

<span data-ttu-id="a382d-104">La semantica per i contesti di [*datagramma*](/windows/desktop/SecGloss/d-gly)o senza connessione è leggermente diversa da quella per i contesti orientati alla connessione.</span><span class="sxs-lookup"><span data-stu-id="a382d-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="a382d-105">Nel [*contesto*](/windows/desktop/SecGloss/c-gly)senza connessione di un datagramma, un server non è in grado di determinare quando il client è stato arrestato o ha interrotto la connessione.</span><span class="sxs-lookup"><span data-stu-id="a382d-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="a382d-106">In altre parole, nessun avviso di terminazione viene passato dall'applicazione di trasporto al server come avviene in un contesto orientato alla connessione.</span><span class="sxs-lookup"><span data-stu-id="a382d-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="a382d-107">Per usare un contesto di datagramma, un client imposta il \_ flag del datagramma di ISC req \_ nella chiamata alla funzione [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="a382d-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a382d-108">Il pacchetto [Microsoft Kerberos](microsoft-kerberos.md) non supporta i contesti di datagramma in modalità utente-utente.</span><span class="sxs-lookup"><span data-stu-id="a382d-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="a382d-109">Per supportare meglio alcuni modelli, in particolare RPC di tipo DCE, le regole seguenti si applicano quando il client usa un contesto di datagramma:</span><span class="sxs-lookup"><span data-stu-id="a382d-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="a382d-110">Il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) non produce un [*BLOB*](/windows/desktop/SecGloss/b-gly) di autenticazione (oggetto binario di grandi dimensioni) nella prima chiamata a [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="a382d-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="a382d-111">Tuttavia, il client può usare il contesto di sicurezza restituito in una chiamata alla funzione [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) per generare una firma per un messaggio.</span><span class="sxs-lookup"><span data-stu-id="a382d-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="a382d-112">Il pacchetto di sicurezza deve consentire il ristabilimento del contesto più volte per consentire al server di eliminare la connessione senza preavviso.</span><span class="sxs-lookup"><span data-stu-id="a382d-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="a382d-113">Ciò implica che le chiavi utilizzate nelle funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) possono essere reimpostate su uno [*stato*](/windows/desktop/SecGloss/s-gly)coerente.</span><span class="sxs-lookup"><span data-stu-id="a382d-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="a382d-114">Il pacchetto di sicurezza consente al chiamante di specificare le informazioni sulla sequenza e fornisce le informazioni sulla sequenza sul lato ricevente.</span><span class="sxs-lookup"><span data-stu-id="a382d-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="a382d-115">In aggiunta alle informazioni sulle sequenze gestite dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a382d-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="a382d-116">Un pacchetto di sicurezza imposta il \_ \_ flag datagramma del flag SECPKG per indicare che supporta la semantica del datagramma.</span><span class="sxs-lookup"><span data-stu-id="a382d-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
