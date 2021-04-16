---
description: La sintassi del messaggio crittografico può essere usata per codificare i messaggi in busta digitale.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codifica dei dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc20fc7483ba1ef364d8b59824d26bd14d458d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555548"
---
# <a name="encoding-enveloped-data"></a>Codifica dei dati in busta

I dati in busta sono costituiti da contenuto crittografato di qualsiasi tipo e chiavi della sessione di crittografia del contenuto crittografate per uno o più destinatari. I messaggi in busta digitale mantengono il contenuto del segreto del messaggio e consentono solo a persone o entità specifiche di recuperare il contenuto.

La sintassi del messaggio crittografico (CMS) può essere usata per codificare i messaggi in busta digitale. CMS supporta tre tecniche di gestione delle chiavi: il trasporto chiavi, il contratto chiave e le chiavi di crittografia chiavi simmetriche distribuite in precedenza. La crittografia KEK simmetrica precedentemente distribuita è nota anche come distribuzione della chiave della lista di distribuzione.

In ognuna di queste tre tecniche viene generata una singola chiave di sessione per crittografare il messaggio in busta digitale. I problemi di gestione delle chiavi riguardano il modo in cui la chiave di sessione viene crittografata dal mittente e decrittografata da un ricevitore. Un singolo messaggio crittografato può essere distribuito a molti destinatari usando una combinazione delle tecniche di gestione delle chiavi.

Per la crittografia della chiave della sessione, la gestione delle chiavi del trasporto chiave usa la chiave pubblica di un destinatario previsto. Il ricevitore decrittografa la chiave della sessione utilizzando la chiave privata associata alla chiave pubblica utilizzata per la crittografia. Il ricevitore usa quindi la chiave della sessione decrittografata per decrittografare i dati in busta. Quando si utilizza il trasporto delle chiavi, il destinatario non ha confermato le informazioni sull'identità del mittente.

Per la gestione dei contratti chiave, viene generata una chiave privata temporanea Diffie-Hellman temporanea che viene usata per crittografare la chiave della sessione. La chiave pubblica corrispondente alla chiave privata temporanea è inclusa come parte delle informazioni sul destinatario del messaggio. Il destinatario decrittografa la chiave della sessione utilizzando la chiave temporanea ricevuta e utilizza la chiave della sessione decrittografata per decrittografare il messaggio in busta digitale. Utilizzando il contratto di chiave temporanea insieme alla chiave privata del ricevitore, il destinatario del messaggio ha confermato le informazioni sull'identità del mittente.

Per la gestione delle chiavi con [*chiavi simmetriche*](../secgloss/s-gly.md)distribuite in precedenza, ogni messaggio include la chiave di crittografia del contenuto crittografata con una chiave di crittografia della chiave distribuita in precedenza. I ricevitori usano la chiave di crittografia della chiave distribuita in precedenza per decrittografare la chiave di crittografia del contenuto e quindi usare la chiave di crittografia del contenuto decrittografata per decrittografare il messaggio in busta digitale.

Nella figura seguente è illustrata una tipica sequenza di eventi CMS per la codifica dei dati in busta.

![codifica dei dati in busta](images/envelmsg.png)

-   Viene recuperato un puntatore al messaggio in [*testo non crittografato*](../secgloss/p-gly.md) .
-   Viene generata una chiave simmetrica ([*sessione*](../secgloss/s-gly.md)).
-   La [*chiave simmetrica*](../secgloss/s-gly.md) e l'algoritmo di crittografia specificato vengono utilizzati per crittografare i dati del messaggio.
-   Viene aperto un [*archivio certificati*](../secgloss/c-gly.md) .
-   Il certificato del destinatario viene recuperato dall'archivio.
-   La [*chiave pubblica*](../secgloss/p-gly.md) viene recuperata dal certificato del destinatario.
-   Utilizzando la chiave pubblica del destinatario, la chiave simmetrica viene crittografata.
-   Dal certificato del destinatario viene recuperato l'ID del destinatario.
-   Le informazioni seguenti sono incluse nel messaggio in busta digitale: l'algoritmo di crittografia dei dati, i dati crittografati, la chiave simmetrica crittografata e la struttura delle informazioni sul destinatario.

Per utilizzare le funzioni di messaggio di basso livello per eseguire le attività tipiche elencate, attenersi alla procedura riportata di seguito.

**Per codificare un messaggio in busta digitale**

1.  Creare o recuperare il contenuto.
2.  Ottenere un provider di crittografia.
3.  Ottenere un certificato del destinatario.
4.  Inizializza la struttura delle [**\_ informazioni di \_ codifica \_ in busta CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) .
5.  Chiamare [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per ottenere la dimensione del BLOB del messaggio codificato. Allocare memoria per l'it.
6.  Chiamare [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG in \_ busta per *dwMsgType* e un puntatore a [**CMSG le \_ informazioni di \_ codifica \_ in busta**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) digitale per *pvMsgEncodeInfo*. In seguito a questa chiamata, verrà visualizzato un handle per il messaggio aperto.
7.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando l'handle recuperato nel passaggio 6 e un puntatore ai dati che devono essere crittografati, in busta e codificati. Questa funzione può essere chiamata il numero di volte necessario per completare il processo di codifica.
8.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 6 e i tipi di parametro appropriati per accedere ai dati codificati desiderati. Ad esempio, passare CMSG \_ Content \_ param per ottenere un puntatore all'intero \# messaggio PKCS 7.

    Se il risultato di questa codifica deve essere usato come [*dati interni*](../secgloss/i-gly.md) per un altro messaggio codificato, ad esempio un messaggio in busta, è \_ \_ necessario passare il parametro CMSG bare Content \_ param. Per un esempio, vedere [codice alternativo per la codifica di un messaggio in busta](alternate-code-for-encoding-an-enveloped-message.md)digitale.

9.  Chiudere il messaggio chiamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Il risultato di questa procedura è un messaggio codificato che contiene i dati crittografati, la [*chiave simmetrica*](../secgloss/s-gly.md) crittografata con le chiavi pubbliche del destinatario e le strutture dei dati delle informazioni sul destinatario. La combinazione di contenuto crittografato e chiave simmetrica crittografata per un destinatario è una [*busta digitale*](../secgloss/d-gly.md) per tale destinatario. Qualsiasi tipo di contenuto può essere bustato per più destinatari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di programma C: codifica di un messaggio firmato in busta](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
