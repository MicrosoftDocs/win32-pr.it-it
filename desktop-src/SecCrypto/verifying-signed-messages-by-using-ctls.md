---
description: Uno dei vantaggi dell'uso degli elenchi di certificati attendibili è che le applicazioni possono essere progettate in modo da verificare automaticamente i messaggi firmati rispetto ai certificati attendibili senza infastidire l'utente con le finestre di dialogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Verifica dei messaggi firmati tramite CCL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624a132ed976800d1c8a8ab0dcd878f533f0d0b947879e87e3e8dc21ccff51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896232"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Verifica dei messaggi firmati tramite CCL

Uno dei vantaggi dell'uso degli elenchi di certificati attendibili [*è*](../secgloss/c-gly.md) che le applicazioni possono essere progettate in modo da verificare automaticamente i messaggi firmati rispetto ai certificati attendibili senza infastidire l'utente con le finestre di dialogo. Fornisce anche a un amministratore di rete le origini di controllo da usare come attendibili.

La procedura seguente può essere usata per verificare la firma di un messaggio firmato tramite un CTL.

**Per verificare un messaggio firmato tramite un CTL**

1.  Decodificare il messaggio come segue:

    1.  Ottenere un puntatore al messaggio ricevuto (BLOB [*codificato).*](../secgloss/b-gly.md)
    2.  Chiamare [**CryptMsgOpenToDecode,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)passando gli argomenti necessari.
    3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio b e un puntatore ai dati da decodificare. In questo modo vengono eseguite le azioni appropriate sul messaggio, a seconda del tipo di messaggio.

2.  Verificare la firma del messaggio decodificato e firmato e ottenere un puntatore a CERT CONTEXT del [**\_ firmatario.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

    Questa operazione può essere eseguita chiamando [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando l'handle di messaggio recuperato nel passaggio 1c come *parametro hCryptMsg.* Se la chiamata di funzione restituisce **TRUE,** la firma è stata verificata e nel parametro *ppSigner* viene restituito un puntatore [**al contesto PCCERT \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmatario.

3.  Verificare che il firmatario sia un'origine attendibile come segue:

    1.  Aprire l'archivio certificati contenente l'elenco CTL appropriato.
    2.  Ottenere un puntatore a [**CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) chiamando [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
    3.  Per verificare che il firmatario sia un'origine attendibile, chiamare [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passando il puntatore recuperato nel passaggio precedente nel parametro *pCtlContext,* CTL CERT SUBJECT TYPE nel parametro dwSubjectType e il puntatore a CERT CONTEXT recuperato nel passaggio \_ \_ \_ 2 nel *parametro pvSubject.* [**\_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)  Se la chiamata di funzione restituisce **TRUE,** **il CERT \_ CONTEXT** passato alla funzione è un'origine attendibile nel CTL.

 

 
