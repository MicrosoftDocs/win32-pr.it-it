---
description: Uno dei vantaggi dell'utilizzo degli elenchi di certificati attendibili (scopi consentiti) è che le applicazioni possono essere progettate in modo da verificare automaticamente i messaggi firmati rispetto ai certificati attendibili senza infastidire l'utente con le finestre di dialogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Verifica dei messaggi firmati tramite scopi consentiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312784"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Verifica dei messaggi firmati tramite scopi consentiti

Uno dei vantaggi dell'utilizzo degli [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti) è che le applicazioni possono essere progettate in modo da verificare automaticamente i messaggi firmati rispetto ai certificati attendibili senza infastidire l'utente con le finestre di dialogo. Consente inoltre di ritenere attendibili le origini di controllo di un amministratore di rete.

È possibile utilizzare la procedura seguente per verificare la firma di un messaggio firmato utilizzando un elenco di scopi consentiti.

**Per verificare un messaggio firmato utilizzando un elenco di scopi consentiti**

1.  Decodificare il messaggio come segue:

    1.  Ottenere un puntatore al messaggio ricevuto (il [*BLOB*](../secgloss/b-gly.md)codificato).
    2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari.
    3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio b e un puntatore ai dati che devono essere decodificati. In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.

2.  Verificare la firma del messaggio decodificato, firmato e ottenere un puntatore al [**\_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)del firmatario.

    Questa operazione può essere eseguita chiamando [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando l'handle di messaggio recuperato nel passaggio 1C come parametro *hCryptMsg* . Se la chiamata di funzione restituisce **true**, la firma è stata verificata e viene restituito un puntatore al [**\_ contesto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmatario nel parametro *ppSigner* .

3.  Verificare che il firmatario sia un'origine attendibile come segue:

    1.  Aprire l'archivio certificati contenente l'elenco di scopi consentiti appropriato.
    2.  Ottenere un puntatore al [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) chiamando [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
    3.  Per confermare che il firmatario è un'origine attendibile, chiamare [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passando il puntatore recuperato nel passaggio precedente nel parametro *pCtlContext* , il \_ tipo di oggetto del certificato CTL \_ \_ nel parametro *dwSubjectType* e il puntatore al [**\_ contesto del certificato**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) recuperato nel passaggio 2 nel parametro *pvSubject* . Se la chiamata di funzione restituisce **true**, **il \_ contesto del certificato** passato alla funzione è un'origine attendibile nell'elenco di scopi consentiti.

 

 
