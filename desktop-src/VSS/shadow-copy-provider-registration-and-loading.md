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
# <a name="shadow-copy-provider-registration-and-loading"></a>Registrazione e caricamento del provider di copie shadow

## <a name="provider-registration"></a>Registrazione del provider

Solo provider di chiamate VSS. Il provider esegue la registrazione per le chiamate richiamando [**IVssAdmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passando l' **\_ \_ hardware VSS prov** per il parametro *eProviderType* . Una volta registrato, il provider verrà usato per la gestione delle copie shadow fino all'annullamento della registrazione con [**IVssAdmin:: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Caricamento e scaricamento del provider

I provider possono essere caricati e scaricati di frequente. I provider possono implementare [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) per determinare quando VSS carica o Scarica il provider.

 

 



