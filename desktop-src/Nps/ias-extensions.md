---
title: Estensioni del server dei criteri di rete
description: L'API delle estensioni NPS consente agli sviluppatori di software di scrivere dll di estensione che possono essere usate per l'autenticazione, l'autorizzazione e l'accounting. L'API delle estensioni NPS supporta il protocollo RADIUS (Remote Authentication Dial-In User Service).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963310"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="71aa0-104">Estensioni del server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="71aa0-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="71aa0-105">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="71aa0-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="71aa0-106">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="71aa0-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="71aa0-107">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="71aa0-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="71aa0-108">L'API delle estensioni NPS consente agli sviluppatori di software di scrivere dll di estensione che possono essere usate per l'autenticazione, l'autorizzazione e l'accounting.</span><span class="sxs-lookup"><span data-stu-id="71aa0-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="71aa0-109">L'API delle estensioni NPS supporta il protocollo RADIUS (Remote Authentication Dial-In User Service).</span><span class="sxs-lookup"><span data-stu-id="71aa0-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="71aa0-110">Le DLL di estensione implementate tramite l'API delle estensioni NPS possono fornire un controllo e una contabilità di sessione avanzati.</span><span class="sxs-lookup"><span data-stu-id="71aa0-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="71aa0-111">Queste dll possono essere utilizzate per scenari quali il controllo del numero di sessioni di rete degli utenti finali, l'utilizzo di un server di stato e la connessione ai database di autenticazione del dominio e ai servizi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71aa0-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="71aa0-112">Le DLL di estensione possono espandere le autorizzazioni di accesso remoto fornite da NPS aggiungendo le proprie autorizzazioni quando si invia una risposta di accettazione a un client di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="71aa0-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="71aa0-113">L'API delle estensioni NPS è applicabile in qualsiasi ambiente informatico in cui potrebbe migliorare l'efficienza per autenticare gli utenti di connessione remota tramite un server remoto.</span><span class="sxs-lookup"><span data-stu-id="71aa0-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="71aa0-114">Questa tecnologia è particolarmente utile per i provider di servizi Internet (ISP).</span><span class="sxs-lookup"><span data-stu-id="71aa0-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="71aa0-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="71aa0-115">In This Section</span></span>

[<span data-ttu-id="71aa0-116">Overview</span><span class="sxs-lookup"><span data-stu-id="71aa0-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="71aa0-117">Informazioni generali su RADIUS e sull'API delle estensioni NPS.</span><span class="sxs-lookup"><span data-stu-id="71aa0-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="71aa0-118">Usando</span><span class="sxs-lookup"><span data-stu-id="71aa0-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="71aa0-119">Codice di esempio che illustra come usare l'API delle estensioni NPS.</span><span class="sxs-lookup"><span data-stu-id="71aa0-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="71aa0-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="71aa0-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="71aa0-121">Documentazione di tipi, funzioni e strutture enumerate che compongono l'API delle estensioni NPS.</span><span class="sxs-lookup"><span data-stu-id="71aa0-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71aa0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71aa0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71aa0-123">Server dei criteri di rete (servizio di autenticazione Internet)</span><span class="sxs-lookup"><span data-stu-id="71aa0-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="71aa0-124">EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="71aa0-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 