---
description: Utilizzare CertMgr per visualizzare certificati, CRL e scopi consentiti da un file o da un archivio certificati, per copiare i certificati in un archivio certificati, per eliminare certificati da un archivio certificati e per salvare i certificati nei file.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Utilizzo di CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308639"
---
# <a name="using-certmgr"></a>Utilizzo di CertMgr

[Certmgr](certmgr.md) può essere utilizzato per visualizzare [*certificati*](../secgloss/c-gly.md), [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) ed [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti) da un file o un archivio certificati, per copiare i certificati in un [*archivio certificati*](../secgloss/c-gly.md), per eliminare certificati da un archivio certificati e per salvare i certificati nei file.

Quando [certmgr](certmgr.md) viene utilizzato senza opzioni, viene visualizzata una procedura guidata di certmgr per guidare l'utente durante l'operazione.

Il file deve essere uno dei tipi seguenti:

-   Un file CTL, CRL o certificate codificato (potrebbe essere codificato in base 64)
-   Un \# file PKCS 7
-   Un file SPC
-   Documento firmato
-   StoreFile serializzato

Negli esempi seguenti vengono utilizzati i comandi [certmgr](certmgr.md) per eseguire attività comuni relative ai certificati.

-   Visualizzare i certificati, i CRL e scopi consentiti da *MyFile. ext*.

    **certmgr** *MyFile. ext*

-   Visualizzare i certificati, i CRL e scopi consentiti dall'archivio di sistema.

    **certmgr-s My**

-   Copiare tutti i certificati, i CRL e scopi consentiti in un file denominato MyFile *. ext* in un nuovo file, denominato *NewFile. ext*.

    **certmgr-Add-All-c** *MyFile. ext* *NewFile. ext*

-   Copiare tutti i certificati, i CRL e scopi consentiti dall'archivio di sistema in un file denominato *NewMyFile. ext*.

    **certmgr-Add-All-c-s My** *NewMyFile. ext*

-   Copiare un certificato con il nome comune *CERT* nell'archivio di sistema in un file denominato *NewCert. cer*.

    **certmgr-Add-c-n** *CERT* **-s My** *NewCert. cer*

-   Eliminare tutti i certificati dall'archivio di sistema.

    **certmgr-del-all-c-s My**

-   Eliminare tutti i scopi consentiti dall'archivio di sistema personale e salvare l'archivio risultante in un file denominato *NewStore. Str*.

    **certmgr-del-all-CTL-s My** *NewStore. Str*

-   Salvare, in un file denominato *NewCert. cer*, un certificato con codifica [*X. 509*](../secgloss/x-gly.md) , che ha il nome comune *CERT* e che si trova nell'archivio certificati radice.

    **certmgr-put-c-n** *CERT* **-s root** *NewCert. cer*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
