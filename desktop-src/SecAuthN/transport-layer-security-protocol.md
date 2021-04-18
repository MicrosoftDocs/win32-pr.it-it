---
description: Schannel supporta le versioni 1,0, 1,1 e 1,2 del protocollo Transport Layer Security (TLS).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocollo TLS (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315858"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="6f349-103">Protocollo TLS (Transport Layer Security)</span><span class="sxs-lookup"><span data-stu-id="6f349-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="6f349-104">Schannel supporta le versioni 1,0, 1,1 e 1,2 del [*protocollo Transport Layer Security (TLS)*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6f349-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="6f349-105">Questo protocollo è uno standard di settore progettato per proteggere la privacy delle informazioni comunicate tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="6f349-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="6f349-106">TLS presuppone che sia in uso un trasporto orientato alla connessione, in genere TCP.</span><span class="sxs-lookup"><span data-stu-id="6f349-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="6f349-107">Il protocollo TLS consente alle applicazioni client/server di rilevare i rischi di sicurezza seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f349-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="6f349-108">Manomissione di messaggi</span><span class="sxs-lookup"><span data-stu-id="6f349-108">Message tampering</span></span>
-   <span data-ttu-id="6f349-109">Intercettazione messaggi</span><span class="sxs-lookup"><span data-stu-id="6f349-109">Message interception</span></span>
-   <span data-ttu-id="6f349-110">Falsificazione del messaggio</span><span class="sxs-lookup"><span data-stu-id="6f349-110">Message forgery</span></span>

<span data-ttu-id="6f349-111">La specifica completa del protocollo TLS è disponibile nel sito Web IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .</span><span class="sxs-lookup"><span data-stu-id="6f349-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="6f349-112">Organizzazione di TLS</span><span class="sxs-lookup"><span data-stu-id="6f349-112">Organization of TLS</span></span>

<span data-ttu-id="6f349-113">Per l'uso di TLS per la comunicazione client/server sono necessari i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f349-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="6f349-114">**Per usare TLS per la comunicazione client/server**</span><span class="sxs-lookup"><span data-stu-id="6f349-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="6f349-115">Negoziazione di handshake e del pacchetto di crittografia</span><span class="sxs-lookup"><span data-stu-id="6f349-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="6f349-116">Autenticazione delle entità</span><span class="sxs-lookup"><span data-stu-id="6f349-116">Authentication of parties</span></span>
3.  <span data-ttu-id="6f349-117">Scambio di informazioni correlate alla chiave</span><span class="sxs-lookup"><span data-stu-id="6f349-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="6f349-118">Scambio di dati dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="6f349-118">Application data exchange</span></span>

<span data-ttu-id="6f349-119">I passaggi che costituiscono TLS sono divisi in due protocolli che, insieme, forniscono la sicurezza della connessione:</span><span class="sxs-lookup"><span data-stu-id="6f349-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="6f349-120">[Protocollo di handshake TLS](tls-handshake-protocol.md)-(passaggi da 1 a 3)</span><span class="sxs-lookup"><span data-stu-id="6f349-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="6f349-121">[Protocollo di record TLS](tls-record-protocol.md)-(passaggio 4)</span><span class="sxs-lookup"><span data-stu-id="6f349-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="6f349-122">SSPI con implementazioni TLS</span><span class="sxs-lookup"><span data-stu-id="6f349-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="6f349-123">Poiché TLS non ha una specifica GSSAPI, i responsabili dell'implementazione di TLS potrebbero non avere familiarità con le funzioni SSPI.</span><span class="sxs-lookup"><span data-stu-id="6f349-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="6f349-124">Le applicazioni chiamano le funzioni SSPI per enumerare i pacchetti disponibili, creare e utilizzare handle per le credenziali, creare contesti di sicurezza e garantire la privacy dell'integrità dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="6f349-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="6f349-125">Per supportare le funzioni SSPI utilizzate dalle applicazioni in modalità utente, le funzioni elencate in [funzioni implementate da SSP/APS in modalità utente](/windows/desktop/SecAuthN/authentication-functions) devono essere supportate dalle implementazioni TLS, ad esempio schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="6f349-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="6f349-126">Per informazioni dettagliate sulle funzioni SSPI e sulle funzioni SSP, vedere [funzioni di autenticazione](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6f349-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f349-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f349-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f349-128">Pacchetti di crittografia TLS</span><span class="sxs-lookup"><span data-stu-id="6f349-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="6f349-129">TLS e SSL</span><span class="sxs-lookup"><span data-stu-id="6f349-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
