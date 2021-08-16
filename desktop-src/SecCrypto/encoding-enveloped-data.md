---
description: La sintassi dei messaggi crittografici può essere usata per codificare i messaggi in busta.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codifica dei dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3517a956311373d067072899ee71bcdf742990877c7d569bfe4e5ef7f2757e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766762"
---
# <a name="encoding-enveloped-data"></a>Codifica dei dati in busta

I dati in busta sono costituiti da contenuto crittografato di qualsiasi tipo e chiavi di sessione di crittografia del contenuto crittografate per uno o più destinatari. I messaggi in busta mantengono il contenuto del segreto del messaggio e consentono solo a persone o entità specificate di recuperare il contenuto.

È possibile usare la sintassi del messaggio crittografico (CMS) per codificare i messaggi in busta. CMS supporta tre tecniche di gestione delle chiavi: trasporto delle chiavi, contratto di chiave e chiavi di crittografia a chiave simmetrica (KEK) distribuite in precedenza. La chiave KEK simmetrica distribuita in precedenza è nota anche come distribuzione della chiave della lista di distribuzione.

In ognuna di queste tre tecniche viene generata una singola chiave di sessione per crittografare il messaggio in busta. I problemi di gestione delle chiavi si occupano del modo in cui la chiave di sessione viene crittografata dal mittente e decrittografata da un ricevitore. Un singolo messaggio crittografato può essere distribuito a molti destinatari usando una combinazione delle tecniche di gestione delle chiavi.

La gestione delle chiavi di trasporto delle chiavi usa la chiave pubblica di un destinatario previsto per crittografare la chiave di sessione. Il ricevitore decrittografa la chiave di sessione usando la chiave privata associata alla chiave pubblica usata per crittografare. Il ricevitore usa quindi la chiave di sessione decrittografata per decrittografare i dati in busta. Quando si usa il trasporto chiave, il ricevitore non ha confermato le informazioni sull'identità del mittente.

Nella gestione dell'accordo chiave viene generata e usata una chiave privata temporanea Diffie-Hellman temporanea per crittografare la chiave di sessione. La chiave pubblica corrispondente alla chiave privata effimera è inclusa come parte delle informazioni sul destinatario del messaggio. Il destinatario decrittografa la chiave di sessione usando la chiave effimera ricevuta e usa questa chiave di sessione decrittografata per decrittografare il messaggio in busta. Usando l'accordo di chiave effimera in combinazione con la chiave privata del destinatario, il destinatario del messaggio ha informazioni confermate sull'identità del mittente.

Per la gestione delle chiavi tramite chiavi [*simmetriche*](../secgloss/s-gly.md)distribuite in precedenza, ogni messaggio include la chiave di crittografia del contenuto crittografata con una chiave di crittografia della chiave distribuita in precedenza. I ricevitori usano la chiave di crittografia della chiave distribuita in precedenza per decrittografare la chiave di crittografia del contenuto, quindi usano la chiave di crittografia del contenuto decrittografata per decrittografare il messaggio in busta.

Nella figura seguente è illustrata una tipica sequenza di eventi CMS per la codifica dei dati in busta.

![codifica dei dati in busta](images/envelmsg.png)

-   Viene recuperato un puntatore al messaggio [*di*](../secgloss/p-gly.md) testo non crittografato.
-   Viene generata una [*chiave*](../secgloss/s-gly.md)simmetrica ( sessione ).
-   La [*chiave simmetrica e*](../secgloss/s-gly.md) l'algoritmo di crittografia specificato vengono usati per crittografare i dati del messaggio.
-   Viene [*aperto un archivio*](../secgloss/c-gly.md) certificati.
-   Il certificato del destinatario viene recuperato dall'archivio.
-   La [*chiave pubblica*](../secgloss/p-gly.md) viene recuperata dal certificato del destinatario.
-   Usando la chiave pubblica del destinatario, la chiave simmetrica viene crittografata.
-   Dal certificato del destinatario viene recuperato l'ID del destinatario.
-   Nel messaggio con busta digitale sono incluse le informazioni seguenti: l'algoritmo di crittografia dei dati, i dati crittografati, la chiave simmetrica crittografata e la struttura delle informazioni sul destinatario.

Per usare le funzioni di messaggi di basso livello per eseguire le attività tipiche appena elencate, usare la procedura seguente.

**Per codificare un messaggio in busta**

1.  Creare o recuperare il contenuto.
2.  Ottenere un provider di crittografia.
3.  Ottenere un certificato del destinatario.
4.  Inizializzare [**la struttura CMSG \_ ENVELOPED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info)
5.  Chiamare [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per ottenere le dimensioni del BLOB del messaggio codificato. Allocare memoria.
6.  Chiamare [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG ENVELOPED per dwMsgType e un puntatore \_ a [**CMSG \_ ENVELOPED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) per *pvMsgEncodeInfo*.  Come risultato di questa chiamata, si otterrà un handle per il messaggio aperto.
7.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando l'handle recuperato nel passaggio 6 e un puntatore ai dati da crittografare, inviluppiare e codificare. Questa funzione può essere chiamata il numero di volte necessario per completare il processo di codifica.
8.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 6 e i tipi di parametro appropriati per accedere ai dati codificati desiderati. Ad esempio, passare CMSG CONTENT PARAM per ottenere un puntatore \_ \_ all'intero messaggio PKCS \# 7.

    Se il risultato di questa codifica [](../secgloss/i-gly.md) deve essere usato come dati interni per un altro messaggio codificato, ad esempio un messaggio con busta, è necessario passare il parametro \_ CMSG BARE \_ CONTENT \_ PARAM. Per un esempio, vedere [Codice alternativo per la codifica di un messaggio in busta](alternate-code-for-encoding-an-enveloped-message.md).

9.  Chiudere il messaggio chiamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Il risultato di questa procedura è un messaggio codificato che contiene i dati crittografati, la chiave simmetrica crittografata con le chiavi pubbliche del destinatario e le strutture di dati delle informazioni sul destinatario. [](../secgloss/s-gly.md) La combinazione di contenuto crittografato e chiave simmetrica crittografata per un destinatario è una [*busta*](../secgloss/d-gly.md) digitale per tale destinatario. Qualsiasi tipo di contenuto può essere in busta per più destinatari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programma C di esempio: codifica di un messaggio con busta e firmato](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
