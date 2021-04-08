---
title: Classe CSecureChannelServer
description: Classe CSecureChannelServer
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Gestione dispositivi, classe CSecureChannelServer
- Gestione dispositivi, classe CSecureChannelServer
- provider di servizi, classe CSecureChannelServer
- Guida di riferimento alla programmazione, classe CSecureChannelServer
- informazioni di riferimento su Windows Media Gestione dispositivi, classe CSecureChannelServer
- Classe CSecureChannelServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727879"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="ba4e9-109">Classe CSecureChannelServer</span><span class="sxs-lookup"><span data-stu-id="ba4e9-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="ba4e9-110">La classe **CSecureChannelServer** è una classe helper (non un'interfaccia) che consente a un provider di servizi o a un provider di contenuti protetto di autenticare un'applicazione usando l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , di crittografare e decrittografare i dati e di creare firme Mac.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="ba4e9-111">Il processo di autenticazione richiede che l'applicazione crei un oggetto **CSecureChannelClient** e che il provider di servizi crei un oggetto **CSecureChannelServer** .</span><span class="sxs-lookup"><span data-stu-id="ba4e9-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="ba4e9-112">Le classi **CSecureChannelClient** e **CSecureChannelServer** sono dichiarate nella libreria a collegamento statico, mssachlp. lib.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="ba4e9-113">Tutti i metodi di Windows Media Gestione dispositivi, provider di servizi e interfacce del provider di contenuti protetti possono restituire WMDM \_ E \_ NOTCERTIFIED per indicare che il chiamante non è stato autenticato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="ba4e9-114">La classe **CSecureChannelServer** espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="ba4e9-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="ba4e9-115">Method</span></span>                                                            | <span data-ttu-id="ba4e9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba4e9-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4e9-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="ba4e9-118">Decrittografa i dati contenuti in un parametro.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="ba4e9-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="ba4e9-120">Crittografa i dati contenuti in un parametro.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="ba4e9-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="ba4e9-122">Verifica che sia stato stabilito correttamente un canale di autenticazione protetto.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="ba4e9-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="ba4e9-124">Recupera i livelli di sicurezza dell'applicazione dei componenti locali e remoti.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="ba4e9-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="ba4e9-126">Recupera la chiave della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="ba4e9-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="ba4e9-128">Rilascia il canale MAC (Message Authentication Code) e recupera un valore MAC finale.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="ba4e9-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="ba4e9-130">Acquisisce un canale MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="ba4e9-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="ba4e9-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="ba4e9-132">Aggiorna il valore del codice MAC (Message Authentication Code) con un valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="ba4e9-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="ba4e9-134">Stabilisce un canale autenticato sicuro tra i componenti.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="ba4e9-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="ba4e9-136">Segnala i protocolli supportati da un componente.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="ba4e9-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="ba4e9-138">Specifica il certificato e la chiave privata del server SAC (Secure Authenticated Channel).</span><span class="sxs-lookup"><span data-stu-id="ba4e9-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="ba4e9-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ba4e9-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="ba4e9-140">Imposta la chiave della sessione utilizzata per comunicare con un altro componente.</span><span class="sxs-lookup"><span data-stu-id="ba4e9-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="ba4e9-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba4e9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4e9-142">**Classe CSecureChannelClient**</span><span class="sxs-lookup"><span data-stu-id="ba4e9-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="ba4e9-143">**Interfaccia IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="ba4e9-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="ba4e9-144">**Interfacce per i provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="ba4e9-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="ba4e9-145">**Uso di canali con autenticazione sicura**</span><span class="sxs-lookup"><span data-stu-id="ba4e9-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 