---
title: Ricezione di traffico non richiesto su Teredo
description: Teredo fornisce connettività globale usando le funzionalità di attraversamento NAT e IPv6.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729042"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="35e6e-103">Ricezione di traffico non richiesto su Teredo</span><span class="sxs-lookup"><span data-stu-id="35e6e-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="35e6e-104">[Teredo](about-teredo.md) fornisce connettività globale usando le funzionalità di attraversamento NAT e IPv6.</span><span class="sxs-lookup"><span data-stu-id="35e6e-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="35e6e-105">Tuttavia, molte applicazioni, tra cui peer-to-peer, richiedono Teredo per ricevere traffico non richiesto da Internet.</span><span class="sxs-lookup"><span data-stu-id="35e6e-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="35e6e-106">Un'applicazione può essere programmata per ricevere traffico su una singola interfaccia IPv6 o su tutte le interfacce che supportano IPv6.</span><span class="sxs-lookup"><span data-stu-id="35e6e-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="35e6e-107">In questa documentazione vengono descritti i requisiti per le applicazioni che utilizzano l'interfaccia Teredo per ricevere traffico IPv6 non richiesto.</span><span class="sxs-lookup"><span data-stu-id="35e6e-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="35e6e-108">Un'applicazione riceverà traffico non richiesto sull'interfaccia Teredo solo se l'applicazione è registrata con [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span><span class="sxs-lookup"><span data-stu-id="35e6e-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="35e6e-109">Per ricevere traffico non richiesto, è necessario che si verifichi quanto segue:</span><span class="sxs-lookup"><span data-stu-id="35e6e-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="35e6e-110">Agli utenti deve essere richiesto di utilizzare Microsoft Management Console (MMC) per abilitare l'opzione "attraversamento confini" per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35e6e-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="35e6e-111">Questa opzione è disponibile in Windows Firewall Snap-In--> <application name> > scheda "avanzate". L'opzione "attraversamento bordo" deve essere abilitata singolarmente per ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="35e6e-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="35e6e-112">L'opzione "attraversamento bordo" è abilitata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35e6e-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="35e6e-113">È possibile che le applicazioni in grado di ricevere traffico non richiesto vengano registrate con Windows Firewall per "attraversamento del perimetro" e ricevano traffico non richiesto sull'interfaccia Teredo.</span><span class="sxs-lookup"><span data-stu-id="35e6e-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="35e6e-114">A tale scopo, un'applicazione deve chiamare l'API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) con l'opzione "attraversamento bordo" impostata su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="35e6e-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="35e6e-115">Il consenso dell'utente è necessario per questa chiamata API prima che un'applicazione sia autorizzata ad ascoltare il traffico.</span><span class="sxs-lookup"><span data-stu-id="35e6e-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="35e6e-116">L'applicazione imposta l'opzione del socket del [ \_ \_ livello di protezione IPv6](/windows/desktop/WinSock/ipv6-protection-level) Winsock sul **livello di protezione \_ \_ senza restrizioni** tramite [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="35e6e-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="35e6e-117">Ciò consentirà all'applicazione di ricevere il traffico di attraversamento perimetrale.</span><span class="sxs-lookup"><span data-stu-id="35e6e-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35e6e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35e6e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35e6e-119">Ricezione di traffico richiesto su Teredo</span><span class="sxs-lookup"><span data-stu-id="35e6e-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 