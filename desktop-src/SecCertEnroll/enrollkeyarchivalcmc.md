---
description: Crea una richiesta di certificato CMC per archiviare una chiave privata in un'autorità di certificazione (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e2e9856309560e982e7e1dda7ba724fefd0759e6fa10196b321eb66947cf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882951"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

L'esempio enrollKeyArchivalCMC crea una richiesta di certificato CMC per archiviare una chiave privata in un'autorità di certificazione (CA). Per altre informazioni, vedere [CMC Key Archival Request](cmc-key-archival-request.md).

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollKeyArchivalCMC .

## <a name="discussion"></a>Discussione

L'esempio enrollKeyArchivalCMC:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello di certificato da usare per la registrazione.
2.  Crea un [**oggetto richiesta di certificato IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza per un contesto dell'utente finale usando il nome del modello.
3.  Imposta la [**proprietà ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) nella richiesta CMC.
4.  Crea un [**oggetto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
5.  Crea un oggetto [**CryptoAPI ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa per recuperare il certificato di scambio per la CA.
6.  Crea un oggetto [**IX509Enrollment,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) lo inizializza usando la richiesta CMC, crea una stringa con codifica Base64 che contiene la richiesta di archiviazione della chiave e la invia alla CA.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta di archiviazione chiavi CMC](cmc-key-archival-request.md)
</dt> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
