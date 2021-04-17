---
title: Abilitazione di Criteri di gruppo
description: Informazioni su come configurare il supplicant abilitando criteri di gruppo. Vedere Considerazioni per i supplicant e visualizzare altre risorse disponibili.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399743"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="59021-104">Abilitazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="59021-104">Enabling Group Policy</span></span>

<span data-ttu-id="59021-105">In questo argomento viene illustrato come configurare il supplicant abilitando criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="59021-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="59021-106">I supplicant EAPHost possono partecipare a criteri di gruppo per consentire a un amministratore di rete di configurare centralmente i computer di rete.</span><span class="sxs-lookup"><span data-stu-id="59021-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="59021-107">Il metodo e il meccanismo preciso con cui il supplicant sceglie di partecipare a criteri di gruppo è a discrezione del supplicante.</span><span class="sxs-lookup"><span data-stu-id="59021-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="59021-108">Esempi di meccanismi per la partecipazione a criteri di gruppo includono estensioni lato client/server, modelli amministrativi e così via.</span><span class="sxs-lookup"><span data-stu-id="59021-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="59021-109">Considerazioni per l'abilitazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="59021-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="59021-110">Queste sono le considerazioni per i supplicant rispetto a criteri di gruppo e EAP.</span><span class="sxs-lookup"><span data-stu-id="59021-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="59021-111">La configurazione EAP deve sempre essere archiviata come XML quando possibile e non nel formato binario.</span><span class="sxs-lookup"><span data-stu-id="59021-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="59021-112">Criteri di gruppo può essere applicato a qualsiasi computer nel dominio e la configurazione del metodo EAP e i dati utente non sono necessariamente portabili tra architetture di processori a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="59021-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="59021-113">Il codice XML risolve i problemi di limite dell'architettura del processore perché il supplicant converte localmente l'XML indipendente dall'architettura del processore alla rappresentazione binaria della configurazione al momento dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="59021-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="59021-114">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="59021-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="59021-115">Domande frequenti generali</span><span class="sxs-lookup"><span data-stu-id="59021-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="59021-116">[Domande frequenti sul metodo EAP](eap-method-frequently-asked-questions.md).</span><span class="sxs-lookup"><span data-stu-id="59021-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="59021-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="59021-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="59021-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="59021-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="59021-119">Se viene utilizzata un'estensione lato server di criteri di gruppo, l'estensione chiamerà in genere [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) per determinare i metodi disponibili e per generare la configurazione EAP appropriata per quel criterio.</span><span class="sxs-lookup"><span data-stu-id="59021-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="59021-120">Il criterio viene quindi inviato ai client di rete appropriati in cui viene applicato il criterio.</span><span class="sxs-lookup"><span data-stu-id="59021-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59021-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59021-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59021-122">Configurazione dell'interfaccia utente del metodo EAP</span><span class="sxs-lookup"><span data-stu-id="59021-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="59021-123">Implementazione del supporto di In-Band NAP per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="59021-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="59021-124">Implementazione del supporto NAP per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="59021-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="59021-125">Trasferimento di dati tra i metodi supplicant e EAP</span><span class="sxs-lookup"><span data-stu-id="59021-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="59021-126">Supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="59021-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




