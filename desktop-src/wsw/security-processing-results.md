---
title: Risultati dell'elaborazione della sicurezza
description: Su un canale sicuro, solo i messaggi che passano correttamente i controlli di sicurezza vengono recapitati all'applicazione.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Servizi Web per i risultati dell'elaborazione della sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300686"
---
# <a name="security-processing-results"></a><span data-ttu-id="2948a-106">Risultati dell'elaborazione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="2948a-106">Security Processing Results</span></span>

<span data-ttu-id="2948a-107">Su un canale sicuro, solo i messaggi che passano correttamente i controlli di sicurezza vengono recapitati all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2948a-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="2948a-108">Per questi messaggi, alcuni risultati della verifica della sicurezza sono allegati come proprietà del messaggio e l'applicazione può estrarre ed esaminare tali proprietà per eseguire passaggi aggiuntivi, ad esempio i controlli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2948a-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="2948a-109">La funzione [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) può essere utilizzata per recuperare tutte le proprietà correlate alla sicurezza definite nell' [**ID della \_ \_ proprietà del \_ messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="2948a-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="2948a-110">**WsGetMessageProperty** restituisce un errore per le query che richiedono proprietà di sicurezza non applicabili al tipo di sicurezza usato sul canale.</span><span class="sxs-lookup"><span data-stu-id="2948a-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="2948a-111">Il messaggio continua a essere proprietario delle proprietà restituite dalla funzione di query.</span><span class="sxs-lookup"><span data-stu-id="2948a-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="2948a-112">I seguenti elementi API vengono usati con i risultati dell'elaborazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2948a-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="2948a-113">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="2948a-113">Enumeration</span></span>                                                                | <span data-ttu-id="2948a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2948a-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2948a-115">**\_ID della \_ proprietà del token di sicurezza WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2948a-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="2948a-116">Definisce le chiavi per i campi e le proprietà che possono essere estratti da un token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2948a-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="2948a-117">Funzione</span><span class="sxs-lookup"><span data-stu-id="2948a-117">Function</span></span>                                                         | <span data-ttu-id="2948a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2948a-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="2948a-119">**WsGetSecurityTokenProperty**</span><span class="sxs-lookup"><span data-stu-id="2948a-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="2948a-120">Estrae un campo o una proprietà da un token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2948a-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="2948a-121">Handle</span><span class="sxs-lookup"><span data-stu-id="2948a-121">Handle</span></span>                                       | <span data-ttu-id="2948a-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2948a-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2948a-123">\_token di sicurezza WS \_</span><span class="sxs-lookup"><span data-stu-id="2948a-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="2948a-124">Handle opaco che rappresenta un token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2948a-124">An opaque handle representing a security token.</span></span> |



 

 

 




