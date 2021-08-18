---
description: Registrazione e caricamento del provider di copie shadow
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registrazione e caricamento del provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb239303884314375ec865e3862d6a65af7de27bd7351a74e92604d06876bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998111"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Registrazione e caricamento del provider di copie shadow

## <a name="provider-registration"></a>Registrazione del provider

Solo VSS chiama i provider. Il provider si registra per le chiamate richiamando [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passando **VSS \_ PROV \_ HARDWARE** per il *parametro eProviderType.* Dopo la registrazione, il provider sarà coinvolto nella gestione delle copie shadow fino all'annullamento della registrazione tramite [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Caricamento e scaricamento del provider

I provider possono essere spesso caricati e scaricati. I provider possono [**implementare IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) per determinare quando VSS sta caricando o scaricando il provider.

 

 



