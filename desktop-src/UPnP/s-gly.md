---
title: S (API UPnP)
description: Contiene i termini correlati a UPnP che iniziano con la lettera S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9386d7946c51bc02e78aa96c36063d22d75d61d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047710"
---
# <a name="s-upnp-apis"></a><span data-ttu-id="d9a56-103">S (API UPnP)</span><span class="sxs-lookup"><span data-stu-id="d9a56-103">S (UPnP APIs)</span></span>

<span data-ttu-id="d9a56-104">Contiene i termini correlati a UPnP che iniziano con la lettera S.</span><span class="sxs-lookup"><span data-stu-id="d9a56-104">Contains UPnP-related terms that begin with the letter S.</span></span>

<span data-ttu-id="d9a56-105">[A](a-gly.md) B [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) i J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="d9a56-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d9a56-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**servizio**</span><span class="sxs-lookup"><span data-stu-id="d9a56-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**service**</span></span>
</dt> <dd>

<span data-ttu-id="d9a56-107">Un servizio è un'unità funzionale logica.</span><span class="sxs-lookup"><span data-stu-id="d9a56-107">A service is a logical functional unit.</span></span> <span data-ttu-id="d9a56-108">I servizi espongono azioni e modellano alcuni o tutti gli Stati di un dispositivo fisico usando variabili di stato.</span><span class="sxs-lookup"><span data-stu-id="d9a56-108">Services expose actions and model some or all of the states of a physical device using state variables.</span></span>

</dd> <dt>

<span data-ttu-id="d9a56-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Descrizione servizio**</span><span class="sxs-lookup"><span data-stu-id="d9a56-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**service description**</span></span>
</dt> <dd>

<span data-ttu-id="d9a56-110">Una descrizione del servizio è un elenco delle azioni fornite da un servizio e delle variabili di stato associate alle azioni.</span><span class="sxs-lookup"><span data-stu-id="d9a56-110">A service description is a list of the actions a service provides, and the state variables associated with the actions.</span></span>

</dd> <dt>

<span data-ttu-id="d9a56-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**oggetto servizio**</span><span class="sxs-lookup"><span data-stu-id="d9a56-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**service object**</span></span>
</dt> <dd>

<span data-ttu-id="d9a56-112">Un oggetto servizio è la rappresentazione dell'API del punto di controllo di un servizio.</span><span class="sxs-lookup"><span data-stu-id="d9a56-112">A service object is the Control Point API representation of a service.</span></span> <span data-ttu-id="d9a56-113">Un oggetto servizio implementa l'interfaccia [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .</span><span class="sxs-lookup"><span data-stu-id="d9a56-113">A service object implements the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d9a56-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**tipo di servizio**</span><span class="sxs-lookup"><span data-stu-id="d9a56-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**service type**</span></span>
</dt> <dd>

<span data-ttu-id="d9a56-115">Un tipo di servizio è un URN che identifica un servizio.</span><span class="sxs-lookup"><span data-stu-id="d9a56-115">A service type is a URN that identifies a service.</span></span> <span data-ttu-id="d9a56-116">Esiste una relazione uno-a-uno tra un modello di servizio UPnP e un tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="d9a56-116">There is a one-to-one relationship between a UPnP service template and a service type.</span></span> <span data-ttu-id="d9a56-117">Alcuni tipi di servizio standard sono definiti dai comitati di lavoro dei forum UPnP.</span><span class="sxs-lookup"><span data-stu-id="d9a56-117">Several standard service types are defined by the UPnP Forum working committees.</span></span> <span data-ttu-id="d9a56-118">I tipi di servizio sono nel formato urn: schemas-UPnP-org: Service: serviceType: Version.</span><span class="sxs-lookup"><span data-stu-id="d9a56-118">The service types are in the form urn:schemas-upnp-org:service:serviceType:version.</span></span> <span data-ttu-id="d9a56-119">Ad esempio, un tipo di servizio scanner potrebbe essere urn: schemas-UPnP-org: Service: scanner: 1.</span><span class="sxs-lookup"><span data-stu-id="d9a56-119">For example, a scanner service type could be urn:schemas-upnp-org:service:scanner:1.</span></span>

<span data-ttu-id="d9a56-120">I fornitori UPnP possono specificare servizi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d9a56-120">UPnP vendors may specify additional services.</span></span> <span data-ttu-id="d9a56-121">Tali servizi sono identificati da urn: Domain-Name: Service: serviceType: Version dove Domain-Name è un nome di dominio registrato per il fornitore.</span><span class="sxs-lookup"><span data-stu-id="d9a56-121">Such services are denoted by urn:domain-name:service:serviceType:version where domain-name is a domain name that is registered to the vendor.</span></span>

</dd> <dt>

<span data-ttu-id="d9a56-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**variabile di stato**</span><span class="sxs-lookup"><span data-stu-id="d9a56-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**state variable**</span></span>
</dt> <dd>

<span data-ttu-id="d9a56-123">Una variabile di stato è una porzione di dati che descrive una parte dello stato di un servizio.</span><span class="sxs-lookup"><span data-stu-id="d9a56-123">A state variable is a piece of data that describes some part of a service's state.</span></span>

</dd> </dl>

 

 




