---
description: Le credenziali sono necessarie per il processo di autenticazione Schannel; sia il client che il server devono ottenere credenziali valide per stabilire un contesto di sicurezza per lo scambio di messaggi. Per un esempio in cui viene illustrata questa procedura, vedere Recupero delle credenziali.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Recupero delle credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756437"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="c28b7-104">Recupero delle credenziali Schannel</span><span class="sxs-lookup"><span data-stu-id="c28b7-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="c28b7-105">Le credenziali sono necessarie per il processo di autenticazione Schannel; sia il client che il server devono ottenere credenziali valide per stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) per lo scambio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="c28b7-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="c28b7-106">Per un esempio in cui viene illustrata questa procedura, vedere [recupero delle credenziali](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="c28b7-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="c28b7-107">L'applicazione ottiene le credenziali chiamando la funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , che restituisce un handle per le credenziali richieste.</span><span class="sxs-lookup"><span data-stu-id="c28b7-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="c28b7-108">Poiché gli handle delle credenziali vengono utilizzati per archiviare le informazioni di configurazione, non è possibile utilizzare lo stesso handle sia per le operazioni sul lato client che sul lato server.</span><span class="sxs-lookup"><span data-stu-id="c28b7-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="c28b7-109">Ciò significa che le applicazioni che supportano le connessioni client e server devono ottenere almeno due handle di credenziali.</span><span class="sxs-lookup"><span data-stu-id="c28b7-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="c28b7-110">In Windows XP, una [**struttura \_ cred Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) specifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c28b7-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="c28b7-111">Un protocollo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="c28b7-111">A security protocol</span></span>
-   <span data-ttu-id="c28b7-112">Crittografie consentite</span><span class="sxs-lookup"><span data-stu-id="c28b7-112">The allowable ciphers</span></span>
-   <span data-ttu-id="c28b7-113">Punti di forza di crittografia minimo e massimo</span><span class="sxs-lookup"><span data-stu-id="c28b7-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="c28b7-114">Un certificato [*X. 509*](../secgloss/x-gly.md) usato per l'autenticazione, necessario per il server, facoltativo per il client, a meno che il server non richieda l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="c28b7-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="c28b7-115">Passare la struttura di [**\_ cred Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (tramite il parametro *PAuthData* ) alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="c28b7-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="c28b7-116">Questa funzione restituisce l'handle delle credenziali necessario per stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c28b7-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="c28b7-117">Per informazioni dettagliate sull'impostazione delle crittografie usate con Schannel, vedere Specifica delle crittografie [Schannel e dei punti di forza di crittografia](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="c28b7-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="c28b7-118">Per informazioni sui certificati, vedere [funzioni di archivio certificati e](../seccrypto/cryptography-functions.md)certificati.</span><span class="sxs-lookup"><span data-stu-id="c28b7-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="c28b7-119">Per un esempio in cui viene illustrata l'apertura di un [*archivio certificati*](../secgloss/c-gly.md) e l'individuazione di un certificato da usare per l'autenticazione Schannel, vedere [ottenere un certificato](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="c28b7-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
