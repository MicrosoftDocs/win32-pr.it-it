---
title: Classi del Gateway Desktop remoto
description: Il provider WMI Gateway Desktop remoto (Gateway Desktop remoto) fornisce le classi seguenti.
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713291"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="5ae42-103">Classi del Gateway Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="5ae42-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="5ae42-104">Il provider WMI Gateway Desktop remoto (Gateway Desktop remoto) fornisce le classi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ae42-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5ae42-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5ae42-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5ae42-106">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="5ae42-107">Rappresenta una connessione da un computer client a un server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-108">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="5ae42-109">Descrive un criterio di autorizzazione della connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="5ae42-110">I tappi RD vengono usati per determinare se un utente è autorizzato a connettersi al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-111">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="5ae42-112">Descrive un set di server di bilanciamento del carico di Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="5ae42-113">Questi vengono usati per il bilanciamento del carico delle connessioni Gateway Desktop remoto su più server.</span><span class="sxs-lookup"><span data-stu-id="5ae42-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-114">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="5ae42-115">Viene descritto un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri di autorizzazione della connessione Servizi Desktop remoto (RD CAPs).</span><span class="sxs-lookup"><span data-stu-id="5ae42-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-116">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="5ae42-117">Descrive un criterio di autorizzazione risorse Desktop remoto (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="5ae42-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="5ae42-118">Un criterio di autorizzazione risorse Desktop remoto viene usato per decidere se un utente è autorizzato a connettersi a una risorsa specificata tramite Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-119">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="5ae42-120">Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi computer) a una singola entità.</span><span class="sxs-lookup"><span data-stu-id="5ae42-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-121">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="5ae42-122">Utilizzato per le operazioni specifiche del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="5ae42-123">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="5ae42-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="5ae42-124">Fornisce metodi e proprietà per visualizzare e configurare le impostazioni del server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5ae42-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




