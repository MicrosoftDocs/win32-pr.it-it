---
description: Una chiave master è il materiale dei dati della chiave da cui derivano altre chiavi.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Creazione della chiave master
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea47c64348f89563340a4e25d411ed3174ee9d18ba1705d9707eab6b39633b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876531"
---
# <a name="creating-the-master-key"></a>Creazione della chiave master

Una [*chiave master è*](../secgloss/m-gly.md) il materiale dei dati della chiave da cui derivano altre chiavi. A seconda del protocollo e della suite di crittografia usata, la chiave master può avere una lunghezza da 5 a 48 byte. Per [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) CSP, la chiave master viene creata dal lato client e trasferita al server in una busta RSA. Per un provider di servizi di configurazione [*Diffie-Hellman/Schannel,*](../secgloss/d-gly.md)la chiave master viene creata eseguendo uno scambio di Diffie-Hellman chiave.

Il codice per la creazione e lo scambio di chiavi master è illustrato in:

-   [Codice client Diffie-Hellman per la creazione della chiave master](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Codice del server Diffie-Hellman per la creazione della chiave master](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Codice client RSA per la creazione della chiave master](rsa-client-code-for-creating-the-master-key.md)
-   [Codice del server RSA per la creazione della chiave master](rsa-server-code-for-creating-the-master-key.md)
-   [Specifica degli algoritmi](specifying-the-algorithms.md)

 

 
