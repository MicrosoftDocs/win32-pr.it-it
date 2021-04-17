---
title: Classe CSecureChannelClient
description: Classe CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Gestione dispositivi, classe CSecureChannelClient
- Gestione dispositivi, classe CSecureChannelClient
- applicazioni desktop, classe CSecureChannelClient
- Guida di riferimento alla programmazione, classe CSecureChannelClient
- informazioni di riferimento su Windows Media Gestione dispositivi, classe CSecureChannelClient
- Classe CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299916"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="fc771-109">Classe CSecureChannelClient</span><span class="sxs-lookup"><span data-stu-id="fc771-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="fc771-110">La classe **CSecureChannelClient** è una classe helper (non un'interfaccia) che consente alle applicazioni di autenticarsi, crittografare e decrittografare i dati e creare i computer Mac.</span><span class="sxs-lookup"><span data-stu-id="fc771-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="fc771-111">La classe **CSecureChannelClient** espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc771-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="fc771-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="fc771-112">Method</span></span>                                                            | <span data-ttu-id="fc771-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc771-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc771-114">[**Autenticare**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc771-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="fc771-115">Attiva lo scambio di certificati tra i componenti per stabilire una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="fc771-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="fc771-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="fc771-117">Consente di decrittografare i dati ricevuti tramite un parametro.</span><span class="sxs-lookup"><span data-stu-id="fc771-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="fc771-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="fc771-119">Crittografa i dati inviati tramite un parametro.</span><span class="sxs-lookup"><span data-stu-id="fc771-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="fc771-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc771-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="fc771-121">Verifica che sia stato stabilito correttamente un canale di autenticazione protetto.</span><span class="sxs-lookup"><span data-stu-id="fc771-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="fc771-122">Questo metodo non viene utilizzato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fc771-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="fc771-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc771-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="fc771-124">Recupera i livelli di sicurezza dell'applicazione dei componenti locali e remoti.</span><span class="sxs-lookup"><span data-stu-id="fc771-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="fc771-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="fc771-126">Recupera la chiave della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="fc771-126">Retrieves the current session key.</span></span> <span data-ttu-id="fc771-127">Questo metodo non viene utilizzato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fc771-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="fc771-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="fc771-129">Rilascia il canale MAC (Message Authentication Code) e recupera un valore MAC finale.</span><span class="sxs-lookup"><span data-stu-id="fc771-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="fc771-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="fc771-131">Acquisisce un canale MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="fc771-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="fc771-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="fc771-133">Aggiunge un valore a un codice MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="fc771-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="fc771-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc771-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="fc771-135">Specifica il certificato e la chiave privata del client del canale autenticato sicuro (SAC).</span><span class="sxs-lookup"><span data-stu-id="fc771-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="fc771-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc771-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="fc771-137">Seleziona l'interfaccia utilizzata per le comunicazioni del canale autenticato (SAC) sicuro.</span><span class="sxs-lookup"><span data-stu-id="fc771-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="fc771-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc771-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="fc771-139">Imposta la chiave della sessione utilizzata per comunicare con un altro componente.</span><span class="sxs-lookup"><span data-stu-id="fc771-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="fc771-140">Questo metodo non viene utilizzato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fc771-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="fc771-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc771-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc771-142">**Classe CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="fc771-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="fc771-143">**Interfaccia IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="fc771-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="fc771-144">**Interfacce per le applicazioni**</span><span class="sxs-lookup"><span data-stu-id="fc771-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 