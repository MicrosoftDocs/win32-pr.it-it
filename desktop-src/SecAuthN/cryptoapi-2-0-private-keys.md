---
description: Le credenziali Schannel sono rappresentate internamente come strutture del contesto del certificato \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: Chiavi private CryptoAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313744"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="25e66-103">Chiavi private CryptoAPI 2.0</span><span class="sxs-lookup"><span data-stu-id="25e66-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="25e66-104">Le credenziali Schannel sono rappresentate internamente come strutture del [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="25e66-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="25e66-105">Schannel individua la [*chiave privata*](/windows/desktop/SecGloss/p-gly) associata a un particolare contesto del certificato usando la \_ Proprietà CERT Key \_ prova \_ info \_ prop \_ ID del certificato.</span><span class="sxs-lookup"><span data-stu-id="25e66-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="25e66-106">Utilizzando questa proprietà, Schannel accede alla *chiave privata* chiamando la funzione [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="25e66-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="25e66-107">Per ulteriori informazioni, vedere [coppie di chiavi pubbliche/private](/windows/desktop/SecCrypto/public-private-key-pairs).</span><span class="sxs-lookup"><span data-stu-id="25e66-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="25e66-108">Ogni credenziale Schannel contiene un riferimento a una o più chiavi private, ciascuna associata a un particolare certificato.</span><span class="sxs-lookup"><span data-stu-id="25e66-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="25e66-109">Le [*chiavi private*](/windows/desktop/SecGloss/p-gly) vengono gestite in modo diverso a seconda che si tratti di una credenziale per un client o un server.</span><span class="sxs-lookup"><span data-stu-id="25e66-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="25e66-110">Chiavi private client</span><span class="sxs-lookup"><span data-stu-id="25e66-110">Client Private Keys</span></span>

<span data-ttu-id="25e66-111">Le [*chiavi private*](/windows/desktop/SecGloss/p-gly) del client vengono gestite dal [*provider del servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP) in uso.</span><span class="sxs-lookup"><span data-stu-id="25e66-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="25e66-112">Le chiavi private del client vengono in genere archiviate da DSN di tipo [prov \_ RSA \_ full](/windows/desktop/SecCrypto/prov-rsa-full) o prov \_ RSA \_ Signature.</span><span class="sxs-lookup"><span data-stu-id="25e66-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="25e66-113">Se l'applicazione client esegue manualmente la chiamata [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) , prima di chiamare [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), il client deve associare l'handle del CSP al contesto del certificato usando la \_ Proprietà CERT Key \_ ID dell' \_ handle \_ prop \_ .</span><span class="sxs-lookup"><span data-stu-id="25e66-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="25e66-114">Se Schannel trova questo set di proprietà, non usa la proprietà CERT \_ Key \_ prov \_ info \_ prop \_ ID.</span><span class="sxs-lookup"><span data-stu-id="25e66-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="25e66-115">Chiavi private del server</span><span class="sxs-lookup"><span data-stu-id="25e66-115">Server Private Keys</span></span>

<span data-ttu-id="25e66-116">Le chiavi private del server vengono archiviate da uno dei CSP seguenti:</span><span class="sxs-lookup"><span data-stu-id="25e66-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="25e66-117">DIMOSTRAZIONE di \_ RSA \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="25e66-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="25e66-118">PROV \_ DH \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="25e66-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="25e66-119">PROVA \_ CSP di fortezza</span><span class="sxs-lookup"><span data-stu-id="25e66-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="25e66-120">La scelta del provider CSP dipende dall'algoritmo di [*scambio delle chiavi*](/windows/desktop/SecGloss/k-gly)selezionato.</span><span class="sxs-lookup"><span data-stu-id="25e66-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="25e66-121">Le chiavi private del server devono essere di tipo in scambio di chiave \_ .</span><span class="sxs-lookup"><span data-stu-id="25e66-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 
