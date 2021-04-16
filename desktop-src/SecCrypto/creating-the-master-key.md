---
description: Una chiave master è un materiale dati chiave da cui derivano altre chiavi.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Creazione della chiave master
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525740"
---
# <a name="creating-the-master-key"></a>Creazione della chiave master

Una [*chiave master*](../secgloss/m-gly.md) è un materiale dati chiave da cui derivano altre chiavi. A seconda del protocollo e del pacchetto di crittografia utilizzati, la chiave master può avere una lunghezza compresa tra 5 e 48 byte. Per il [](../secgloss/r-gly.md) / CSP [*Schannel*](../secgloss/s-gly.md) RSA, la chiave master viene creata dal lato client e trasferita al server in una busta RSA. Per un CSP/SChannel di [*Diffie-Hellman*](../secgloss/d-gly.md), la chiave master viene creata eseguendo uno scambio di chiave Diffie-Hellman.

Il codice per la creazione e lo scambio di chiavi master è illustrato in:

-   [Codice client Diffie-Hellman per la creazione della chiave master](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Codice server Diffie-Hellman per la creazione della chiave master](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Codice client RSA per la creazione della chiave master](rsa-client-code-for-creating-the-master-key.md)
-   [Codice server RSA per la creazione della chiave master](rsa-server-code-for-creating-the-master-key.md)
-   [Specifica degli algoritmi](specifying-the-algorithms.md)

 

 
