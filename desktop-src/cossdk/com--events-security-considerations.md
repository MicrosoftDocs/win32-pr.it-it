---
description: Quando si utilizza il servizio eventi COM+, è possibile eseguire alcune operazioni per garantire che le informazioni riservate contenute in un evento non vengano compromesse.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Considerazioni sulla sicurezza degli eventi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966381"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="b76f7-103">Considerazioni sulla sicurezza degli eventi COM+</span><span class="sxs-lookup"><span data-stu-id="b76f7-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="b76f7-104">Quando si utilizza il servizio eventi COM+, è possibile eseguire alcune operazioni per garantire che le informazioni riservate contenute in un evento non vengano compromesse.</span><span class="sxs-lookup"><span data-stu-id="b76f7-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="b76f7-105">Gli autori di eventi devono tenere presente che tutte le parti in grado di scrivere nel catalogo COM+ possono sottoscrivere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b76f7-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="b76f7-106">Se pertanto le informazioni contenute in un oggetto classe di evento sono sensibili, è necessario utilizzare lo strumento di amministrazione Servizi componenti per verificare che le comunicazioni con i sottoscrittori siano crittografate per l'applicazione che contiene i componenti della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="b76f7-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="b76f7-107">Nella scheda **sicurezza** della finestra delle proprietà dell'applicazione com+ selezionare **pacchetto privacy** come **livello di autenticazione per le chiamate** impostazione. Inoltre, è necessario utilizzare i [filtri eventi](filtering-events-in-com-.md) per garantire che gli eventi vengano recapitati solo ai sottoscrittori appropriati.</span><span class="sxs-lookup"><span data-stu-id="b76f7-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="b76f7-108">I sottoscrittori di eventi devono tenere presente che un utente malintenzionato con accesso alla rete e conoscere l'oggetto della classe di evento potrebbe creare falsi eventi.</span><span class="sxs-lookup"><span data-stu-id="b76f7-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="b76f7-109">È quindi consigliabile usare la [sicurezza basata sui ruoli](role-based-security-administration.md) per garantire che i chiamanti dei metodi dell'oggetto della classe di evento dispongano delle credenziali appropriate per eseguire le azioni descritte dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="b76f7-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="b76f7-110">Per proteggere sia i Publisher che i sottoscrittori, utilizzare il servizio eventi COM+ in una rete privata di host attendibili che è isolata da Internet da un firewall.</span><span class="sxs-lookup"><span data-stu-id="b76f7-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b76f7-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b76f7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b76f7-112">Sicurezza COM+</span><span class="sxs-lookup"><span data-stu-id="b76f7-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="b76f7-113">Filtro di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="b76f7-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="b76f7-114">Oggetto della classe di evento COM+</span><span class="sxs-lookup"><span data-stu-id="b76f7-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



