---
description: Come creare una connessione sicura usando Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Creazione di una connessione sicura mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757292"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="bf92a-103">Creazione di una connessione sicura mediante Schannel</span><span class="sxs-lookup"><span data-stu-id="bf92a-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="bf92a-104">Il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) Schannel fornisce l'accesso a quattro [*protocolli di sicurezza*](/windows/desktop/SecGloss/s-gly):</span><span class="sxs-lookup"><span data-stu-id="bf92a-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="bf92a-105">Transport Layer Security (TLS 1,2)</span><span class="sxs-lookup"><span data-stu-id="bf92a-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="bf92a-106">Transport Layer Security (TLS 1,1)</span><span class="sxs-lookup"><span data-stu-id="bf92a-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="bf92a-107">Transport Layer Security (TLS 1,0)</span><span class="sxs-lookup"><span data-stu-id="bf92a-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="bf92a-108">Secure Sockets Layer (SSL 3,0)</span><span class="sxs-lookup"><span data-stu-id="bf92a-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="bf92a-109">Secure Sockets Layer (SSL 2,0)</span><span class="sxs-lookup"><span data-stu-id="bf92a-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="bf92a-110">I protocolli PCT e SSL 2,0 sono stati sostituiti dal protocollo TLS e non devono essere usati per il nuovo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="bf92a-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="bf92a-111">**Per configurare una connessione sicura tra un client e un server**</span><span class="sxs-lookup"><span data-stu-id="bf92a-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="bf92a-112">Ottenere le credenziali Schannel ([ottenendo le credenziali Schannel](obtaining-schannel-credentials.md)).</span><span class="sxs-lookup"><span data-stu-id="bf92a-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="bf92a-113">Creare un contesto di sicurezza Schannel ([creando un contesto di sicurezza Schannel](creating-an-schannel-security-context.md)).</span><span class="sxs-lookup"><span data-stu-id="bf92a-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="bf92a-114">Una volta stabilita una connessione, è possibile recuperare informazioni sugli attributi.</span><span class="sxs-lookup"><span data-stu-id="bf92a-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="bf92a-115">Per informazioni dettagliate, vedere [ottenere informazioni sulle connessioni Schannel](getting-information-about-schannel-connections.md).</span><span class="sxs-lookup"><span data-stu-id="bf92a-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="bf92a-116">Se, dopo aver stabilito una connessione, i requisiti di sicurezza dell'applicazione cambiano o la connessione viene persa, è possibile rinegoziare la connessione.</span><span class="sxs-lookup"><span data-stu-id="bf92a-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="bf92a-117">Per informazioni dettagliate, vedere [rinegoziazione di una connessione Schannel](renegotiating-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf92a-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="bf92a-118">Al termine dell'utilizzo di una connessione Schannel, è necessario eseguire la pulizia necessaria.</span><span class="sxs-lookup"><span data-stu-id="bf92a-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="bf92a-119">Per informazioni dettagliate, vedere [chiusura di una connessione Schannel](shutting-down-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf92a-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="bf92a-120">Per informazioni sugli esempi forniti con Platform Software Development Kit (SDK) che illustrano il [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly)Schannel, vedere gli esempi di PSDK con Schannel.</span><span class="sxs-lookup"><span data-stu-id="bf92a-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf92a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf92a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf92a-122">Specificare le crittografie Schannel e i punti di forza della crittografia</span><span class="sxs-lookup"><span data-stu-id="bf92a-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
