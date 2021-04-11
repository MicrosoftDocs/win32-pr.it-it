---
title: Descrizione della sicurezza
description: Un Descrizione di sicurezza è rappresentato da una \_ \_ struttura di descrizione della sicurezza WS e viene fornita un'istanza di una descrizione di sicurezza quando si chiama la funzione WsCreateChannel per creare un canale sicuro o la funzione WsCreateListener per creare un listener.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Servizi Web per la descrizione della sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104132134"
---
# <a name="security-description"></a><span data-ttu-id="948b1-106">Descrizione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="948b1-106">Security Description</span></span>

<span data-ttu-id="948b1-107">Un Descrizione di sicurezza è rappresentato da una struttura di [**\_ \_ Descrizione della sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e viene fornita un'istanza di una descrizione di sicurezza quando si chiama la funzione [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) per creare un canale sicuro o la funzione [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) per creare un listener.</span><span class="sxs-lookup"><span data-stu-id="948b1-107">A security desciption is represented by a [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure, and an instance of a security description is supplied when you call the [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) function to create a secure channel or the [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) function to create a listener.</span></span>


## <a name="structure-of-a-security-description"></a><span data-ttu-id="948b1-108">Struttura di una descrizione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="948b1-108">Structure of a Security Description</span></span>

<span data-ttu-id="948b1-109">Il modello di base della sicurezza del canale è che un canale è protetto da uno o più token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="948b1-109">The basic model of channel security is that a channel is secured with one or more security tokens.</span></span> <span data-ttu-id="948b1-110">Riflettendo questo modello, la struttura di [**\_ \_ Descrizione della sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contiene un elenco di associazioni di sicurezza, rappresentate dalle strutture di [**\_ \_ associazione di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , e ogni associazione di sicurezza descrive il modo in cui un token di sicurezza viene ottenuto e utilizzato sul canale.</span><span class="sxs-lookup"><span data-stu-id="948b1-110">Reflecting this model, the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure contains a list of security bindings, represented by [**WS\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) structures, and each security binding describes how one security token is obtained and used on the channel.</span></span> <span data-ttu-id="948b1-111">Il tipo di sicurezza utilizzato su un canale è determinato dalla selezione dei sottotipi di associazione di sicurezza inclusi nella descrizione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="948b1-111">The kind of security used on a channel is decided by the selection of security binding subtypes that are included in the security description.</span></span>

<span data-ttu-id="948b1-112">Le impostazioni di sicurezza facoltative specifiche di un'associazione di sicurezza sono specificate come [impostazioni di associazione](security-binding-settings.md) di sicurezza nella struttura di associazione di sicurezza. Tuttavia, le impostazioni a livello di canale indipendenti dalle associazioni di sicurezza vengono specificate direttamente come [impostazioni del canale di sicurezza](security-channel-settings.md) nel campo **Proprietà** della descrizione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="948b1-112">Optional security settings that are specific to a security binding are specified as [security binding settings](security-binding-settings.md) in the security binding structure; however, channel-wide settings independent of security bindings are directly specified as [security channel settings](security-channel-settings.md) in the **properties** field of the security description itself.</span></span>

![Diagramma che illustra la struttura di una descrizione di sicurezza.](images/securitydescription.png)

<span data-ttu-id="948b1-114">Gli elementi API seguenti vengono usati con le descrizioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="948b1-114">The following API elements are used with security descriptions.</span></span>

| <span data-ttu-id="948b1-115">Struttura</span><span class="sxs-lookup"><span data-stu-id="948b1-115">Structure</span></span>                                                    | <span data-ttu-id="948b1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="948b1-116">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="948b1-117">**\_Descrizione della sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="948b1-117">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | <span data-ttu-id="948b1-118">Struttura di primo livello utilizzata per specificare i requisiti di sicurezza per un canale (sul lato client) o un listener (sul lato server).</span><span class="sxs-lookup"><span data-stu-id="948b1-118">The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).</span></span> |



 

 

 




