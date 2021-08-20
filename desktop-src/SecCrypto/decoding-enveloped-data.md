---
description: Attività generali necessarie per decodificare un messaggio in busta.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodifica dei dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df9df80b2a4bc1e3c9d6894bc83624908468edb63f7d0283ee3dca1b50a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767811"
---
# <a name="decoding-enveloped-data"></a>Decodifica dei dati in busta

Le attività generali necessarie per decodificare un messaggio in busta sono illustrate nella figura seguente e descritte nell'elenco che segue.

![decodifica di dati in busta](images/decemsg.png)

La sequenza di eventi per la decodifica dei dati in busta usando la gestione delle chiavi di trasporto delle chiavi, come illustrato nella figura precedente, è la seguente:

-   Viene recuperato un [*puntatore al*](../secgloss/d-gly.md) messaggio in busta digitale.
-   Viene [*aperto un archivio*](../secgloss/c-gly.md) certificati.
-   Dal messaggio viene recuperato l'ID destinatario (ID).
-   L'ID destinatario viene usato per recuperare il certificato.
-   Viene [*recuperata*](../secgloss/p-gly.md) la chiave privata associata al certificato.
-   La chiave privata viene usata per decrittografare [*la chiave simmetrica*](../secgloss/s-gly.md) ([*sessione*](../secgloss/s-gly.md)).
-   L'algoritmo di crittografia viene recuperato dal messaggio.
-   Usando la chiave privata e l'algoritmo di crittografia, i dati vengono decrittografati.

Nella procedura seguente vengono utilizzate funzioni di messaggi di basso livello per eseguire le attività appena elencate.

**Per decodificare un messaggio in busta**

1.  Ottiene un puntatore al BLOB codificato.
2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)passando gli argomenti necessari.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati da decodificare. In questo modo vengono eseguite le azioni appropriate sul messaggio, a seconda del tipo di messaggio.
4.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 2 e CMSG TYPE PARAM per verificare che il messaggio sia \_ del tipo di dati in \_ busta.
5.  Chiamare di [**nuovo CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)passando CMSG INNER CONTENT TYPE PARAM per ottenere il tipo di dati \_ del contenuto \_ \_ \_ [*interno.*](../secgloss/i-gly.md)
6.  Se il tipo di dati del contenuto interno **è data**, procedere con la decrittografia e la decodifica del contenuto. In caso contrario, eseguire una procedura di decodifica appropriata per il tipo di dati del contenuto.
7.  Supponendo che il tipo di contenuto interno sia "data", inizializzare la struttura dei dati [**CMSG \_ CTRL \_ DECRYPT \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) e chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)passando CMSG CTRL DECRYPT e l'indirizzo della \_ \_ struttura. Il contenuto verrà decrittografato.
8.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)passando CMSG CONTENT PARAM per ottenere un puntatore al BLOB dei dati di contenuto decodificato \_ \_ **(stringa BYTE).**
9.  Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.

Il risultato di questa procedura è che il messaggio viene decodificato e decrittografato e viene recuperato un puntatore al BLOB dei dati del contenuto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programma C di esempio: codifica di un messaggio in busta, firmato](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
