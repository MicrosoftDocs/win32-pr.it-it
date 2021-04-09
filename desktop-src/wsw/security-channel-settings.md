---
title: Impostazioni del canale di sicurezza
description: Le impostazioni del canale di sicurezza controllano il modo in cui la sicurezza viene applicata e verificata su un canale.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Servizi Web per le impostazioni del canale di sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118682"
---
# <a name="security-channel-settings"></a><span data-ttu-id="5c77d-106">Impostazioni del canale di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5c77d-106">Security Channel Settings</span></span>

<span data-ttu-id="5c77d-107">Le impostazioni del canale di sicurezza controllano il modo in cui la sicurezza viene applicata e verificata su un canale.</span><span class="sxs-lookup"><span data-stu-id="5c77d-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="5c77d-108">Ogni impostazione del canale di sicurezza è rappresentata da una raccolta di coppie proprietà-valore, con le chiavi di proprietà definite dall' [**\_ ID della \_ proprietà \_ di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5c77d-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="5c77d-109">Ogni proprietà della raccolta ha un valore predefinito ragionevole.</span><span class="sxs-lookup"><span data-stu-id="5c77d-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="5c77d-110">A causa di questi valori predefiniti, è possibile definire e utilizzare una descrizione di sicurezza senza specificare alcuna impostazione del canale di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5c77d-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="5c77d-111">[Le impostazioni di associazione di sicurezza](security-binding-settings.md) contengono raccolte simili di coppie proprietà-valore le cui chiavi sono definite dalla struttura della proprietà di [**\_ \_ associazione \_ di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) .</span><span class="sxs-lookup"><span data-stu-id="5c77d-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="5c77d-112">La differenza tra questi due tipi di impostazioni è che le impostazioni del canale di sicurezza hanno come ambito una descrizione della sicurezza (ovvero contengono proprietà di sicurezza a livello di canale), mentre le impostazioni di associazione di sicurezza hanno come ambito una delle associazioni di sicurezza e potrebbero esserci numerose associazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5c77d-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="5c77d-113">Di conseguenza, ad esempio, una descrizione di sicurezza personalizzata che contiene tre associazioni di sicurezza avrà un elenco di impostazioni del canale di sicurezza per l'intero canale e tre contenitori delle impostazioni di associazione di sicurezza, uno per ogni associazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5c77d-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="5c77d-114">Con le impostazioni del canale di sicurezza vengono utilizzate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c77d-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="5c77d-115">**\_livello di protezione WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="5c77d-116">**\_ID della \_ proprietà del token di sicurezza WS Request \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="5c77d-117">**\_ \_ ID algoritmo di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="5c77d-118">**\_ID della \_ proprietà dell'algoritmo di sicurezza WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="5c77d-119">**\_layout dell' \_ intestazione di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="5c77d-120">**\_versione dell' \_ intestazione di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="5c77d-121">**\_ID della \_ proprietà di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="5c77d-122">**\_ \_ utilizzo timestamp di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="5c77d-123">**\_ID della \_ proprietà del token di sicurezza WS XML \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="5c77d-124">Con le impostazioni del canale di sicurezza vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c77d-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="5c77d-125">**\_proprietà del \_ token di sicurezza WS Request \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="5c77d-126">**\_ \_ Proprietà algoritmo di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="5c77d-127">**\_suite di \_ algoritmi di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="5c77d-128">**\_proprietà di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="5c77d-129">**\_proprietà del \_ token di sicurezza WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c77d-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




