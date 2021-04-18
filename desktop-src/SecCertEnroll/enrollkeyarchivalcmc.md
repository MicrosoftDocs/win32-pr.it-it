---
description: Crea una richiesta di certificato CMC per archiviare una chiave privata in un'autorità di certificazione (CA).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308113"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

L'esempio enrollKeyArchivalCMC crea una richiesta di certificato CMC per archiviare una chiave privata in un'autorità di certificazione (CA). Per altre informazioni, vedere [richiesta di archiviazione delle chiavi CMC](cmc-key-archival-request.md).

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollKeyArchivalCMC

## <a name="discussion"></a>Discussione

Esempio enrollKeyArchivalCMC:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello di certificato da usare per la registrazione.
2.  Crea un oggetto richiesta di certificato [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza per un contesto dell'utente finale usando il nome del modello.
3.  Imposta la proprietà [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) nella richiesta CMC.
4.  Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
5.  Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa per recuperare il certificato di Exchange per l'autorità di certificazione.
6.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , lo inizializza usando la richiesta CMC, crea una stringa con codifica Base64 che contiene la richiesta di archiviazione delle chiavi e la invia alla CA.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta di archiviazione delle chiavi CMC](cmc-key-archival-request.md)
</dt> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
