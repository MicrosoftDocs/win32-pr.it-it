---
description: Diverse funzioni aggiungono un contesto del certificato o un collegamento a un contesto a un \[ SDK (Software Development Kit) della piattaforma di archiviazione \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Utilizzo dei certificati negli archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347661"
---
# <a name="working-with-certificates-in-certificate-stores"></a>Utilizzo dei certificati negli archivi certificati

Diverse funzioni aggiungono un contesto di certificato o un collegamento a un contesto in un archivio.

Per i certificati già presenti nel formato del contesto del certificato:

-   [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

Per i certificati con formato codificato ma non per i contesti di certificato completi:

-   [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

Le funzioni seguenti eliminano un certificato, un CRL o un elenco di scopi consentiti da un archivio diminuendo di uno il conteggio dei riferimenti. Se il conteggio dei riferimenti diventa zero, viene liberata la memoria utilizzata per archiviare il certificato, l'elenco CRL o l'elenco di scopi consentiti.

-   [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



