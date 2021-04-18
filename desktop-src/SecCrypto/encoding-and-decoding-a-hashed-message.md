---
description: Descrive le attività necessarie per codificare un messaggio con hash.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codifica e decodifica di un messaggio con hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316184"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codifica e decodifica di un messaggio con hash

I dati con hash sono costituiti da contenuto di qualsiasi tipo e da un [*hash*](../secgloss/h-gly.md) del contenuto. Può essere utilizzato quando è necessario solo confermare che il contenuto del messaggio non è stato modificato dopo la creazione dell'hash.

Quando si crea un messaggio con hash, possono essere presenti più algoritmi hash e più hash. Nella figura seguente sono illustrate le attività necessarie per codificare un messaggio con hash. La procedura viene descritta nel testo che segue la figura.

![creazione di un messaggio con hash](images/hashmsg.png)

**Per creare un messaggio con hash**

1.  Ottiene un puntatore ai dati di cui eseguire l'hashing.
2.  Selezionare l'algoritmo hash da utilizzare.
3.  Inserire i dati tramite una funzione di hashing usando l'algoritmo hash.
4.  Includere i dati originali per cui eseguire l'hashing, gli algoritmi hash e gli hash nel messaggio codificato.

Per utilizzare le funzioni di messaggio di basso livello per completare le attività descritte, attenersi alla procedura riportata di seguito.

**Per eseguire l'hashing e codificare un messaggio utilizzando funzioni di messaggio di basso livello**

1.  Consente di creare o recuperare il contenuto di cui eseguire l'hashing.
2.  Ottenere un provider di crittografia.
3.  Inizializza la struttura delle [**\_ informazioni di \_ codifica \_ con hash CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) .
4.  Chiamare [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per ottenere la dimensione del BLOB del messaggio codificato. Allocare memoria per l'it.
5.  Chiamare [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG con \_ hash per il parametro *dwMsgType* e un puntatore a [**CMSG \_ Hashed \_ Encode \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) per il parametro *pvMsgEncodeInfo* . In seguito a questa chiamata, si ottiene un handle per il messaggio aperto.
6.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando l'handle recuperato nel passaggio 5 e un puntatore ai dati per i quali viene eseguito l'hashing e la codifica. Questa funzione può essere chiamata il numero di volte necessario per completare il processo di codifica.
7.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 5 e i tipi di parametro appropriati per accedere ai dati codificati desiderati. Ad esempio, passare CMSG \_ Content \_ param per ottenere un puntatore all'intero messaggio [*PKCS \# 7*](../secgloss/p-gly.md) .

    Se il risultato di questa codifica deve essere usato come [*dati interni*](../secgloss/i-gly.md) per un altro messaggio codificato, ad esempio un messaggio in busta, è \_ \_ necessario passare il param di contenuto bare CMSG \_ . Per un esempio che illustra questo problema, vedere [codice alternativo per la codifica di un messaggio in busta](alternate-code-for-encoding-an-enveloped-message.md)digitale.

8.  Chiudere il messaggio chiamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Il risultato di questa procedura è un messaggio codificato che contiene i dati originali, gli algoritmi di hash e l' [*hash*](../secgloss/h-gly.md) di tali dati. Un puntatore al [*BLOB*](../secgloss/b-gly.md) del messaggio codificato viene ottenuto nel passaggio 7.

Le due procedure seguenti decodificano e quindi verificano i dati con hash.

**Per decodificare i dati con hash**

1.  Ottenere un puntatore al BLOB codificato.
2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando gli argomenti necessari.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati che devono essere decodificati. In questo modo vengono eseguite le azioni appropriate per il messaggio, a seconda del tipo di messaggio.
4.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 2 e i tipi di parametro appropriati per accedere ai dati desiderati e decodificati. Ad esempio, passare CMSG \_ Content \_ param per ottenere un puntatore al contenuto decodificato.

**Per verificare l'hash**

1.  Chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passando CMSG \_ CTRL \_ Verify \_ hash per verificare gli hash.
2.  Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.

Per un programma di esempio, vedere [esempio di programma C: codifica e decodifica di un messaggio con hash](example-c-program-encoding-and-decoding-a-hashed-message.md).

 

 
