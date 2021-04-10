---
title: Interfacce del Gateway Desktop remoto
description: L'API Gateway Desktop remoto (Gateway Desktop remoto) supporta le interfacce seguenti. È possibile usare queste interfacce per implementare plug-in che forniscono l'autenticazione e l'autorizzazione personalizzate.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955199"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="ff14b-104">Interfacce del Gateway Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ff14b-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="ff14b-105">L'API Gateway Desktop remoto (Gateway Desktop remoto) supporta le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff14b-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="ff14b-106">È possibile usare queste interfacce per implementare plug-in che forniscono l'autenticazione e l'autorizzazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ff14b-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="ff14b-107">Non esiste alcuna dipendenza tra il plug-in di autenticazione e il plug-in di autorizzazione ed è possibile implementare un solo plug-in, se si sceglie.</span><span class="sxs-lookup"><span data-stu-id="ff14b-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="ff14b-108">I plug-in di autenticazione sono [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) e [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span><span class="sxs-lookup"><span data-stu-id="ff14b-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="ff14b-109">I plug-in di autorizzazione sono [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)e [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span><span class="sxs-lookup"><span data-stu-id="ff14b-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ff14b-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ff14b-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ff14b-111">**ITSGAccountingEngine**</span><span class="sxs-lookup"><span data-stu-id="ff14b-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="ff14b-112">Espone metodi che forniscono informazioni sulla creazione o la chiusura di sessioni per una connessione.</span><span class="sxs-lookup"><span data-stu-id="ff14b-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ff14b-113">**ITSGAuthenticateUserSink**</span><span class="sxs-lookup"><span data-stu-id="ff14b-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="ff14b-114">Espone metodi che inviano notifiche a Gateway Desktop remoto sugli eventi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ff14b-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="ff14b-115">**ITSGAuthenticationEngine**</span><span class="sxs-lookup"><span data-stu-id="ff14b-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="ff14b-116">Espone metodi che autenticano gli utenti per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ff14b-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="ff14b-117">**ITSGAuthorizeConnectionSink**</span><span class="sxs-lookup"><span data-stu-id="ff14b-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="ff14b-118">Espone metodi che notificano a Gateway Desktop remoto il risultato di un tentativo di autorizzare una connessione.</span><span class="sxs-lookup"><span data-stu-id="ff14b-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ff14b-119">**ITSGAuthorizeResourceSink**</span><span class="sxs-lookup"><span data-stu-id="ff14b-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="ff14b-120">Espone metodi che notificano a Gateway Desktop remoto il risultato di un tentativo di autorizzare una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ff14b-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="ff14b-121">**ITSGPolicyEngine**</span><span class="sxs-lookup"><span data-stu-id="ff14b-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="ff14b-122">Espone metodi che autorizzano connessioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="ff14b-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




