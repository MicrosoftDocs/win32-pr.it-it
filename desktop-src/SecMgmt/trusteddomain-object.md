---
description: L'oggetto TrustedDomain archivia le informazioni su una relazione di trust con un dominio.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Oggetto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878941"
---
# <a name="trusteddomain-object"></a>Oggetto TrustedDomain

L'oggetto **trustedDomain** archivia le informazioni su una relazione di trust con un dominio. Un oggetto **trustedDomain** viene creato nel sistema trusting per identificare un account all'interno del dominio trusted che può essere utilizzato per inviare richieste di autenticazione ed eseguire altre operazioni, ad esempio le conversioni di nome e [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID).

Le informazioni archiviate in un oggetto **trustedDomain** includono:

-   SID del dominio attendibile. Queste informazioni non sono modificabili e devono essere univoche tra tutti gli oggetti **trustedDomain** .
-   Nome del dominio attendibile. Queste informazioni non sono modificabili e devono essere univoche tra tutti gli oggetti **trustedDomain** .
-   Nome dell'account nel dominio trusted utilizzato per inviare le richieste di autenticazione e per eseguire traduzioni di nome e SID. Questo nome non è modificabile.
-   Password utilizzata per inviare richieste di autenticazione ed eseguire traduzioni di nome e SID.

Per ulteriori informazioni, vedere [il tipo di oggetto trustedDomain](the-trusteddomain-object-type.md).

 

 
