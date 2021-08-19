---
description: Illustra le attività necessarie per codificare un messaggio con hash.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codifica e decodifica di un messaggio con hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bed6ffae240d9139de471f16dcaaf2ed3e29d5bc92c8d7507b981c2af67541c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766743"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codifica e decodifica di un messaggio con hash

I dati con hash sono costituiti da contenuto di qualsiasi tipo e [*da un hash*](../secgloss/h-gly.md) del contenuto. Può essere usato solo quando è necessario verificare che il contenuto del messaggio non sia stato modificato dopo la creazione dell'hash.

Quando si crea un messaggio con hash, possono essere presenti più algoritmi hash e più hash. La figura seguente illustra le attività necessarie per codificare un messaggio con hash. La procedura è descritta nel testo che segue l'illustrazione.

![creazione di un messaggio con hash](images/hashmsg.png)

**Per creare un messaggio con hash**

1.  Ottenere un puntatore ai dati di cui eseguire l'hashing.
2.  Consente di selezionare l'algoritmo hash da utilizzare.
3.  Inserire i dati tramite una funzione hash usando l'algoritmo hash .
4.  Includere i dati originali di cui eseguire l'hashing, gli algoritmi hash e gli hash nel messaggio codificato.

Per usare le funzioni di messaggi di basso livello per eseguire le attività appena descritte, usare la procedura seguente.

**Per eseguire l'hashing e la codifica di un messaggio usando funzioni di messaggi di basso livello**

1.  Creare o recuperare il contenuto di cui eseguire l'hashing.
2.  Ottenere un provider del servizio di crittografia.
3.  Inizializzare [**la struttura CMSG \_ HASHED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info)
4.  Chiamare [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per ottenere le dimensioni del BLOB del messaggio codificato. Allocare memoria.
5.  Chiamare [**CryptMsgOpenToEncode,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)passando CMSG HASHED per il parametro \_ *dwMsgType e* un puntatore a [**CMSG \_ HASHED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) per il *parametro pvMsgEncodeInfo.* In seguito a questa chiamata, si ottiene un handle per il messaggio aperto.
6.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)passando l'handle recuperato nel passaggio 5 e un puntatore ai dati di cui eseguire l'hashing e la codifica. Questa funzione può essere chiamata il numero di volte necessario per completare il processo di codifica.
7.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)passando l'handle recuperato nel passaggio 5 e i tipi di parametro appropriati per accedere ai dati codificati desiderati. Ad esempio, passare CMSG CONTENT PARAM per ottenere un puntatore \_ \_ all'intero [*messaggio PKCS \# 7.*](../secgloss/p-gly.md)

    Se il risultato di questa codifica [](../secgloss/i-gly.md) deve essere utilizzato come dati interni per un altro messaggio codificato, ad esempio un messaggio in busta, è necessario passare CMSG \_ BARE \_ CONTENT \_ PARAM. Per un esempio che illustra questa operazione, vedere [Codice alternativo per la codifica di un messaggio in busta.](alternate-code-for-encoding-an-enveloped-message.md)

8.  Chiudere il messaggio chiamando [**CryptMsgClose.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)

Il risultato di questa procedura è un messaggio codificato che contiene i dati originali, gli algoritmi hash e [*l'hash*](../secgloss/h-gly.md) di tali dati. Un puntatore al [*BLOB*](../secgloss/b-gly.md) del messaggio codificato viene ottenuto nel passaggio 7.

Le due procedure seguenti decodificano e quindi verificano i dati con hash.

**Per decodificare i dati con hash**

1.  Ottiene un puntatore al BLOB codificato.
2.  Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)passando gli argomenti necessari.
3.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una volta, passando l'handle recuperato nel passaggio 2 e un puntatore ai dati da decodificare. In questo modo vengono eseguite le azioni appropriate sul messaggio, a seconda del tipo di messaggio.
4.  Chiamare [**CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)passando l'handle recuperato nel passaggio 2 e i tipi di parametro appropriati per accedere ai dati decodificati desiderati. Ad esempio, passare CMSG \_ CONTENT \_ PARAM per ottenere un puntatore al contenuto decodificato.

**Per verificare l'hash**

1.  Chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)passando CMSG \_ CTRL VERIFY HASH per verificare gli \_ \_ hash.
2.  Chiamare [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) per chiudere il messaggio.

Per un programma di esempio, vedere [Programma C di esempio: codifica e decodifica di un messaggio con hash.](example-c-program-encoding-and-decoding-a-hashed-message.md)

 

 
