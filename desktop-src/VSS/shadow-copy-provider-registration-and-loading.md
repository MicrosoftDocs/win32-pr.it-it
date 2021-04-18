---
description: Registrazione e caricamento del provider di copie shadow
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registrazione e caricamento del provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345001"
---
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="b969e-103">Registrazione e caricamento del provider di copie shadow</span><span class="sxs-lookup"><span data-stu-id="b969e-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="b969e-104">Registrazione del provider</span><span class="sxs-lookup"><span data-stu-id="b969e-104">Provider Registration</span></span>

<span data-ttu-id="b969e-105">Solo provider di chiamate VSS.</span><span class="sxs-lookup"><span data-stu-id="b969e-105">Only VSS calls providers.</span></span> <span data-ttu-id="b969e-106">Il provider esegue la registrazione per le chiamate richiamando [**IVssAdmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passando l' **\_ \_ hardware VSS prov** per il parametro *eProviderType* .</span><span class="sxs-lookup"><span data-stu-id="b969e-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="b969e-107">Una volta registrato, il provider verrà usato per la gestione delle copie shadow fino all'annullamento della registrazione con [**IVssAdmin:: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span><span class="sxs-lookup"><span data-stu-id="b969e-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="b969e-108">Caricamento e scaricamento del provider</span><span class="sxs-lookup"><span data-stu-id="b969e-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="b969e-109">I provider possono essere caricati e scaricati di frequente.</span><span class="sxs-lookup"><span data-stu-id="b969e-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="b969e-110">I provider possono implementare [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) per determinare quando VSS carica o Scarica il provider.</span><span class="sxs-lookup"><span data-stu-id="b969e-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



