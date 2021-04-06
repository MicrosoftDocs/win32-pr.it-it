---
title: Strutture di servizi di distribuzione Windows
description: Con servizi di distribuzione Windows vengono utilizzate le strutture seguenti.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045212"
---
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="c5acd-103">Strutture di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="c5acd-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="c5acd-104">Con servizi di distribuzione Windows vengono utilizzate le strutture seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5acd-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="c5acd-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="c5acd-105">Structure</span></span>                                                                         | <span data-ttu-id="c5acd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5acd-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5acd-107">**\_Indirizzo PXE**</span><span class="sxs-lookup"><span data-stu-id="c5acd-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="c5acd-108">Specifica l'indirizzo di rete per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c5acd-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="c5acd-109">**\_messaggio DHCP \_ PXE**</span><span class="sxs-lookup"><span data-stu-id="c5acd-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="c5acd-110">Questa struttura viene utilizzata con l'API del server PXE di servizi di distribuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="c5acd-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="c5acd-111">**PXE \_ ( \_ opzione DHCP)**</span><span class="sxs-lookup"><span data-stu-id="c5acd-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="c5acd-112">Questa struttura viene utilizzata con l'API del server PXE di servizi di distribuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="c5acd-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="c5acd-113">**\_provider PXE**</span><span class="sxs-lookup"><span data-stu-id="c5acd-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="c5acd-114">Descrive un provider.</span><span class="sxs-lookup"><span data-stu-id="c5acd-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="c5acd-115">**\_cred dell'interfaccia della riga di comando WDS \_**</span><span class="sxs-lookup"><span data-stu-id="c5acd-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="c5acd-116">Contiene le credenziali utilizzate per autorizzare una sessione client.</span><span class="sxs-lookup"><span data-stu-id="c5acd-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="c5acd-117">**\_richiesta TRANSPORTCLIENT di WDS \_**</span><span class="sxs-lookup"><span data-stu-id="c5acd-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="c5acd-118">Usato dalla funzione [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .</span><span class="sxs-lookup"><span data-stu-id="c5acd-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="c5acd-119">**\_informazioni sulla sessione TRANSPORTCLIENT \_**</span><span class="sxs-lookup"><span data-stu-id="c5acd-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="c5acd-120">Usato dalla funzione di callback [*\_ WdsTransportClientSessionStartEx di PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) .</span><span class="sxs-lookup"><span data-stu-id="c5acd-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="c5acd-121">**\_ \_ parametri init di WDS TRANSPORTPROVIDER \_**</span><span class="sxs-lookup"><span data-stu-id="c5acd-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="c5acd-122">Usato dalla funzione di callback [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="c5acd-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="c5acd-123">**\_Impostazioni TRANSPORTPROVIDER \_ WDS**</span><span class="sxs-lookup"><span data-stu-id="c5acd-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="c5acd-124">Usato dalla funzione di callback [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="c5acd-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="c5acd-125">Il codice seguente è disponibile a partire da Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c5acd-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="c5acd-126">Struttura</span><span class="sxs-lookup"><span data-stu-id="c5acd-126">Structure</span></span>                                          | <span data-ttu-id="c5acd-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5acd-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="c5acd-128">**PXE \_ ( \_ opzione DHCPV6)**</span><span class="sxs-lookup"><span data-stu-id="c5acd-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="c5acd-129">Utilizzato con l'API del server PXE di servizi di distribuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="c5acd-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="c5acd-130">**\_Messaggio DHCPV6 \_ PXE**</span><span class="sxs-lookup"><span data-stu-id="c5acd-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="c5acd-131">Messaggio DHCPV6.</span><span class="sxs-lookup"><span data-stu-id="c5acd-131">A DHCPV6 message.</span></span>                                         |



 

 

 




