---
description: LSA archivia le informazioni sui criteri di sicurezza locali in un set di oggetti. L'applicazione può eseguire query o modificare i criteri di sicurezza locali accedendo a questi oggetti.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Oggetti criteri LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967613"
---
# <a name="lsa-policy-objects"></a>Oggetti criteri LSA

LSA archivia le informazioni sui criteri di sicurezza locali in un set di oggetti. L'applicazione può eseguire query o modificare i criteri di sicurezza locali accedendo a questi oggetti.

Il set è costituito dai quattro oggetti seguenti:

-   Il [criterio](policy-object.md) contiene informazioni sui criteri globali.
-   [TrustedDomain](trusteddomain-object.md) contiene informazioni su un dominio trusted.
-   L' [account](account-object.md) contiene informazioni su un account utente, gruppo o gruppo locale.
-   [I dati privati](private-data-object.md) contengono informazioni protette, ad esempio le password degli account server. Queste informazioni vengono archiviate come stringhe crittografate.

Per ulteriori informazioni sull'utilizzo delle funzioni dei criteri LSA per gestire le informazioni archiviate in questi oggetti, vedere [utilizzo dei criteri LSA](using-lsa-policy.md).

 

 



