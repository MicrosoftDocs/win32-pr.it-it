---
description: L'helper IP fornisce informazioni sulla configurazione di rete del computer locale.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Recupero di informazioni sulla configurazione di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968397"
---
# <a name="retrieving-information-about-network-configuration"></a>Recupero di informazioni sulla configurazione di rete

L'helper IP fornisce informazioni sulla configurazione di rete del computer locale. Per recuperare le informazioni di configurazione generali, utilizzare la funzione [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Questa funzione restituisce informazioni non specifiche di una particolare scheda o interfaccia. Ad esempio, **GetNetworkParams** restituisce un elenco dei server DNS utilizzati dal computer locale.

-   Per esempi di codice che coinvolgono [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , vedere [recupero di informazioni con GetNetworkParams](retrieving-information-using-getnetworkparams.md).

 

 



