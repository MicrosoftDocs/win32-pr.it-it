---
title: Interfacce del provider Remote Desktop Protocol
description: Interfacce supportate dall'API del provider Remote Desktop Protocol.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955058"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="21a66-103">Interfacce del provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="21a66-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="21a66-104">Le interfacce seguenti sono supportate dall'API del provider Remote Desktop Protocol.</span><span class="sxs-lookup"><span data-stu-id="21a66-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="21a66-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="21a66-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="21a66-106">**IWRdsProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="21a66-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="21a66-107">Espone i metodi chiamati dal servizio Servizi Desktop remoto per configurare una connessione client.</span><span class="sxs-lookup"><span data-stu-id="21a66-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-108">**IWRdsProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="21a66-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="21a66-109">Espone metodi che forniscono informazioni sullo stato di una connessione client e che eseguono azioni per il client.</span><span class="sxs-lookup"><span data-stu-id="21a66-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="21a66-110">Questa interfaccia viene implementata dal servizio Servizi Desktop remoto e chiamata dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="21a66-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-111">**IWRdsProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="21a66-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="21a66-112">Espone i metodi utilizzati dal servizio Servizi Desktop remoto per eseguire l'handshake delle licenze durante una sequenza di connessione.</span><span class="sxs-lookup"><span data-stu-id="21a66-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-113">**IWRdsProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="21a66-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="21a66-114">Espone i metodi che richiedono che il protocollo avvii e arresti l'ascolto delle richieste di connessione client.</span><span class="sxs-lookup"><span data-stu-id="21a66-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-115">**IWRdsProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="21a66-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="21a66-116">Espone metodi che notificano al servizio Servizi Desktop remoto che un client è connesso.</span><span class="sxs-lookup"><span data-stu-id="21a66-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-117">**IWRdsProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="21a66-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="21a66-118">Espone i metodi chiamati dal servizio Servizi Desktop remoto per aggiornare lo stato di accesso e determinare come indirizzare i messaggi di errore di accesso.</span><span class="sxs-lookup"><span data-stu-id="21a66-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-119">**IWRdsProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="21a66-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="21a66-120">Espone metodi che il servizio Servizi Desktop remoto utilizza per comunicare con il provider del protocollo.</span><span class="sxs-lookup"><span data-stu-id="21a66-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-121">**IWRdsProtocolSettings**</span><span class="sxs-lookup"><span data-stu-id="21a66-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="21a66-122">Espone metodi per il recupero e l'aggiunta di impostazioni relative ai criteri.</span><span class="sxs-lookup"><span data-stu-id="21a66-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-123">**IWRdsProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="21a66-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="21a66-124">Espone i metodi chiamati dal protocollo per notificare al servizio Servizi Desktop remoto di avviare o arrestare il lato di destinazione di un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="21a66-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-125">**IWRdsProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="21a66-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="21a66-126">Espone metodi che notificano al provider del protocollo lo stato di shadowing della sessione.</span><span class="sxs-lookup"><span data-stu-id="21a66-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-127">**IWRdsRemoteFXGraphicsConnection**</span><span class="sxs-lookup"><span data-stu-id="21a66-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="21a66-128">Espone metodi relativi alla manipolazione e alla comprensione della grafica nella connessione client.</span><span class="sxs-lookup"><span data-stu-id="21a66-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="21a66-129">Interfacce del provider di protocollo desktop deprecate</span><span class="sxs-lookup"><span data-stu-id="21a66-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="21a66-130">Le interfacce seguenti sono state deprecate e non devono più essere utilizzate.</span><span class="sxs-lookup"><span data-stu-id="21a66-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="21a66-131">Per i nuovi progetti, usare invece le interfacce del provider di Remote Desktop Protocol.</span><span class="sxs-lookup"><span data-stu-id="21a66-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="21a66-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21a66-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a66-133">Riferimento al provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="21a66-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="21a66-134">Enumerazioni del provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="21a66-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="21a66-135">Strutture del provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="21a66-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="21a66-136">Unioni provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="21a66-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




