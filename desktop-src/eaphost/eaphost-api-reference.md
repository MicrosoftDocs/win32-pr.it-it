---
title: Informazioni di riferimento sulle API EAPHost
description: Informazioni sulle API EAPHost e sui relativi componenti. Vedere informazioni di riferimento per vari argomenti sulle API, ad esempio EAPHost XML Schema.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399707"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="195c3-104">Informazioni di riferimento sulle API EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-104">EAPHost API Reference</span></span>

<span data-ttu-id="195c3-105">Le API EAPHost sono divise in tre componenti: le API supplicant, che possono essere richiamate direttamente da un'applicazione abilitata per EAP. API del metodo peer EAP, che gestiscono le richieste dei supplicant per uno specifico tipo di autenticazione EAP e generano elementi interattivi nel client. e le API di autenticazione EAP, che eseguono l'autenticazione sul lato server di un supplicant.</span><span class="sxs-lookup"><span data-stu-id="195c3-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="195c3-106">Gli ultimi due componenti API, ovvero il metodo peer EAP e le API del metodo di autenticazione EAP, richiedono un'implementazione personalizzata e conforme nelle DLL che li espongono al servizio EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="195c3-107">Non possono essere chiamate direttamente dal codice dell'applicazione. vengono invece chiamati da EAPHost (sul lato client per i metodi peer EAP e sul lato server per i metodi di autenticazione EAP) se l'implementazione corrisponde alle firme dell'API specificate nella documentazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="195c3-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="195c3-108">In ogni pagina di riferimento alle funzioni vengono fornite informazioni specifiche sull'implementazione dell'API.</span><span class="sxs-lookup"><span data-stu-id="195c3-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="195c3-109">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="195c3-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="195c3-110">Topic</span></span>                                                      | <span data-ttu-id="195c3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="195c3-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="195c3-112">Impostazioni del registro di sistema EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="195c3-113">Descrive le chiavi del registro di sistema utilizzate da EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="195c3-114">XML Schema EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="195c3-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="195c3-115">Topic</span></span>                                            | <span data-ttu-id="195c3-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="195c3-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="195c3-117">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="195c3-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="195c3-118">Descrive lo schema EAPHost e lo schema legacy per la creazione di XML di configurazione e delle credenziali XML.</span><span class="sxs-lookup"><span data-stu-id="195c3-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="195c3-119">Informazioni di riferimento sulle API EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="195c3-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="195c3-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="195c3-120">Topic</span></span>                                                                   | <span data-ttu-id="195c3-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="195c3-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="195c3-122">Enumerazioni API EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="195c3-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="195c3-123">Elenca le costanti comuni a tutte le API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="195c3-124">Strutture API EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="195c3-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="195c3-125">Elenca le strutture comuni a tutte le API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="195c3-126">Costanti API EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="195c3-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="195c3-127">Elenca le costanti comuni a tutte le API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="195c3-128">Informazioni di riferimento sulle API EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-128">EAPHost API Reference</span></span>



| <span data-ttu-id="195c3-129">Argomento</span><span class="sxs-lookup"><span data-stu-id="195c3-129">Topic</span></span>                                                                       | <span data-ttu-id="195c3-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="195c3-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="195c3-131">Informazioni di riferimento sull'API del richiedente EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="195c3-132">Vengono descritti gli elementi dell'API disponibili per abilitare le chiamate di supplicant a EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="195c3-133">Riferimento all'API del metodo peer EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="195c3-134">Vengono descritti gli elementi API che devono essere implementati per creare una DLL del metodo peer EAP che può essere caricata e chiamata da un client EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="195c3-135">API del metodo di autenticazione EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="195c3-136">Vengono descritti gli elementi API che devono essere implementati per creare una DLL del metodo di autenticazione EAP che può essere caricata e chiamata da un server EAPHost.</span><span class="sxs-lookup"><span data-stu-id="195c3-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="195c3-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="195c3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="195c3-138">Informazioni su EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="195c3-139">Uso di EAPHost</span><span class="sxs-lookup"><span data-stu-id="195c3-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




