---
description: Le funzioni CertAddCertificateLinkToStore, CertAddCRLLinkToStore e CertAddCTLLinkToStore aggiungono collegamenti a contesti esistenti in archivi certificati anziché aggiungere copie di tali contesti.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Collegamenti al certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131446"
---
# <a name="certificate-links"></a>Collegamenti al certificato

Le funzioni [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)e [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) aggiungono collegamenti a contesti esistenti in [*archivi certificati*](../secgloss/c-gly.md) anziché aggiungere copie di tali contesti. L'aggiunta di collegamenti agli archivi rende disponibile lo stesso [*certificato*](../secgloss/c-gly.md)fisico, [*CRL*](../secgloss/c-gly.md)o [*CTL*](../secgloss/c-gly.md) tramite diversi archivi. Le modifiche apportate alle proprietà estese di un [*contesto*](../secgloss/c-gly.md) dall'archivio del contesto originale o da un archivio in cui è archiviato un collegamento a tale contesto sono disponibili nell'archivio che contiene il contesto originale e in tutti gli altri archivi che contengono collegamenti a tale contesto.

Per un esempio in cui viene usato [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), vedere il [programma C di esempio: operazioni sull'archivio certificati](example-c-program-certificate-store-operations.md).

![collegamenti al certificato](images/mancert1.png)

Si supponga che i certificati A. 1, A. 2, A. 3 e A. 4 siano originariamente nel negozio A e che i certificati B. 1, B. 2, B. 3 e B. 4 siano originariamente inclusi nello Store B.

-   Il diagramma mostra un collegamento aggiunto nell'archivio B al certificato A. 2 e un collegamento aggiunto nell'archivio a al certificato B. 2.
-   L'originale del certificato A. 2 è ancora nell'archivio A. L'originale di B. 2 è ancora nell'archivio B.
-   Tutte le modifiche apportate alle proprietà estese del certificato A. 2 o del certificato B. 2 dall'archivio A o dall'archivio B saranno disponibili per entrambi i punti vendita.
-   Se una copia del certificato A. 3 è stata effettuata e archiviata nell'archivio B, qualsiasi modifica apportata alle proprietà estese del certificato originale A. 3 creato dall'archivio A non sarà visibile nella nuova copia nell'archivio B. Se sono state apportate modifiche alle proprietà estese della copia del certificato A. 3 nell'archivio B, tali modifiche non influiranno sul contenuto del certificato originale A. 3 e non saranno visibili dall'archivio A.

 

 
