---
description: L'interfaccia di programmazione ad hoc wireless è costituita dalle interfacce seguenti.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfacce ad hoc wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309438"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="f240d-103">Interfacce ad hoc wireless</span><span class="sxs-lookup"><span data-stu-id="f240d-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="f240d-104">L'interfaccia di programmazione ad hoc wireless è costituita dalle interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="f240d-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="f240d-105">Interface Name (Nome interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f240d-105">Interface Name</span></span>                                                                       | <span data-ttu-id="f240d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f240d-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f240d-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="f240d-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="f240d-108">Rappresenta una scheda di interfaccia di rete wireless (NIC).</span><span class="sxs-lookup"><span data-stu-id="f240d-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="f240d-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="f240d-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="f240d-110">Definisce le notifiche supportate da [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span><span class="sxs-lookup"><span data-stu-id="f240d-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="f240d-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="f240d-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="f240d-112">Crea e gestisce 802,11 reti ad hoc.</span><span class="sxs-lookup"><span data-stu-id="f240d-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="f240d-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="f240d-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="f240d-114">Definisce le notifiche supportate dall'interfaccia [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) .</span><span class="sxs-lookup"><span data-stu-id="f240d-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="f240d-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="f240d-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="f240d-116">Rappresenta una destinazione di rete ad hoc disponibile nell'intervallo di connessione.</span><span class="sxs-lookup"><span data-stu-id="f240d-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="f240d-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="f240d-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="f240d-118">Definisce le notifiche supportate dall'interfaccia [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) .</span><span class="sxs-lookup"><span data-stu-id="f240d-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="f240d-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="f240d-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="f240d-120">Specifica le impostazioni di sicurezza per una rete ad hoc wireless.</span><span class="sxs-lookup"><span data-stu-id="f240d-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="f240d-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="f240d-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="f240d-122">Rappresenta la raccolta di interfacce di rete ad hoc 802,11 attualmente visibili.</span><span class="sxs-lookup"><span data-stu-id="f240d-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="f240d-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="f240d-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="f240d-124">Rappresenta la raccolta di reti ad hoc 802,11 attualmente visibili.</span><span class="sxs-lookup"><span data-stu-id="f240d-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="f240d-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="f240d-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="f240d-126">Rappresenta la raccolta di impostazioni di sicurezza associate a ogni rete wireless ad hoc visibile.</span><span class="sxs-lookup"><span data-stu-id="f240d-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="f240d-127">La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="f240d-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="f240d-128">A partire da Windows 8.1 e Windows Server 2012 R2, usare invece [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="f240d-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



