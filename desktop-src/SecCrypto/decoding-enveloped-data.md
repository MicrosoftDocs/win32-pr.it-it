---
description: Attività generali necessarie per decodificare un messaggio in busta digitale.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodifica dei dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565894"
---
# <a name="decoding-enveloped-data"></a>Decodifica dei dati in busta

Le attività generali necessarie per decodificare un messaggio in busta digitale sono illustrate nella figura seguente e descritte nell'elenco che segue.

![decodifica dei dati in busta](images/decemsg.png)

La sequenza di eventi per la decodifica dei dati in busta con la gestione delle chiavi di trasporto chiave, come illustrato nella figura precedente, è la seguente:

-   Viene recuperato un puntatore al messaggio in [*busta digitale*](../secgloss/d-gly.md) .
-   Viene aperto un [*archivio certificati*](../secgloss/c-gly.md) .
-   Dal messaggio, viene recuperato l'ID del destinatario (ID).
-   L'ID del destinatario viene usato per recuperare il certificato.
-   Viene recuperata la [*chiave privata*](../secgloss/p-gly.md) associata al certificato.
-   La chiave privata viene utilizzata per decrittografare la chiave [*simmetrica*](../secgloss/s-gly.md) ([*sessione*](../secgloss/s-gly.md)).
-   L'algoritmo di crittografia viene recuperato dal messaggio.
-   Utilizzando la chiave privata e l'algoritmo di crittografia, i dati vengono decrittografati.

Nella procedura seguente vengono utilizzate le funzioni di messaggio di basso livello per eseguire le attività elencate.

**Per decodificare un messaggio in busta digitale**

1.  Ottenere un puntatore al BLOB codificato.
2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati che devono essere decodificati. In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.
4.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 2 e CMSG \_ di tipo \_ param per verificare che il messaggio sia del tipo di dati con envelope.
5.  Chiamare di nuovo [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando \_ il parametro del tipo di contenuto interno CMSG \_ \_ \_ per ottenere il tipo di dati del [*contenuto interno*](../secgloss/i-gly.md).
6.  Se il tipo di dati del contenuto interno è **dati**, continuare a decrittografare e decodificare il contenuto. In caso contrario, eseguire una procedura di decodifica appropriata per il tipo di dati content.
7.  Supponendo che il tipo di contenuto interno sia "data", inizializzare la struttura [**CMSG \_ CTRL \_ Decrypt \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data e chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CMSG \_ CTRL \_ Decrypt e l'indirizzo della struttura. Il contenuto verrà decrittografato.
8.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando \_ il parametro di contenuto CMSG \_ per ottenere un puntatore al BLOB di dati del contenuto decodificato (stringa di **byte** ).
9.  Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.

Il risultato di questa procedura è che il messaggio viene decodificato e decrittografato e viene recuperato un puntatore al BLOB di dati del contenuto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di programma C: codifica di un messaggio firmato in busta](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
