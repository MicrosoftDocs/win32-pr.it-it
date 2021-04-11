---
description: Descrive la procedura per la codifica di un messaggio firmato.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codifica dei dati firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232937"
---
# <a name="encoding-signed-data"></a>Codifica dei dati firmati

[*I dati firmati*](../secgloss/s-gly.md) sono costituiti da contenuto di qualsiasi tipo e [*hash*](../secgloss/h-gly.md) di messaggi crittografati del contenuto per zero o più firmatari. L'hash risultante può confermare che il messaggio originale non è stato modificato dopo la firma e che le persone o entità specifiche hanno firmato i dati.

Nella figura seguente viene illustrata la procedura per la codifica di un messaggio firmato. L'elenco seguente illustra i passaggi.

Un messaggio può avere più firmatari, algoritmi di hashing e certificati. Mentre nell'illustrazione vengono mostrati solo i certificati, i [*CRL*](../secgloss/c-gly.md)e [*scopi consentiti*](../secgloss/c-gly.md) possono utilizzare lo stesso processo. Si adattano all'illustrazione quando vengono visualizzati i certificati.

![codifica di un messaggio firmato](images/signmsg2.png)

Il processo generale per la codifica [*dei dati firmati*](../secgloss/s-gly.md) è il seguente.

**Per codificare i dati firmati**

1.  I dati vengono creati (se necessario) e viene recuperato un puntatore a tale oggetto.
2.  Viene aperto un [*archivio certificati*](../secgloss/c-gly.md) che contiene il certificato del firmatario.
3.  Viene recuperata la chiave privata per il certificato. È necessario impostare due proprietà sul certificato prima di utilizzarlo. Una viene utilizzata per associare un certificato a un particolare CSP e, all'interno di tale CSP, a un [*contenitore di chiavi*](../secgloss/k-gly.md)private specifico. L'altro viene usato per indicare quale algoritmo di hash deve essere usato quando viene chiamata un'operazione [*hash*](../secgloss/h-gly.md) . Questi devono essere impostati solo una volta.
4.  La proprietà di un certificato determina l'algoritmo hash.
5.  Un hash dei dati viene creato inviando i dati tramite la funzione hash.
6.  La firma viene creata crittografando l'hash usando la chiave privata, ottenuta tramite una proprietà nel certificato.
7.  I dati seguenti sono inclusi nel messaggio firmato completato:
    -   Dati originali da firmare
    -   Algoritmi hash
    -   Firme
    -   Strutture di informazioni sul firmatario, che include l'identificatore del firmatario (autorità emittente del certificato e numero di serie)
    -   Certificati del firmatario (facoltativo)

In questa procedura viene illustrato un caso semplice. Casi più complessi coinvolgono gli attributi autenticati inclusi nel messaggio. Quando il tipo di contenuto è qualsiasi ma una stringa di **byte** oppure esiste almeno un attributo autenticato insieme a qualsiasi tipo di dati, sono necessari due attributi autenticati standard: il tipo di contenuto (dati) e l'hash del contenuto. In queste circostanze, [*CryptoAPI*](../secgloss/c-gly.md) fornisce automaticamente questi due attributi obbligatori. Le funzioni di messaggio di basso livello eseguono l'hashing degli attributi autenticati, crittografano l'hash con la chiave privata e lo forniscono come firma.

Usare le funzioni di messaggio di basso livello per eseguire le attività elencate, usando la procedura seguente.

**Per codificare un messaggio firmato**

1.  Creare o recuperare il contenuto.
2.  Ottenere un provider di crittografia.
3.  Ottenere i certificati del firmatario.
4.  Inizializza la struttura delle [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) .
5.  Inizializza la struttura delle [**\_ informazioni di \_ codifica \_ CMSG firmate**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
6.  Chiamare [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per ottenere la dimensione del BLOB del messaggio codificato. Allocare memoria per l'it.
7.  Chiamare [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG \_ firmato per *dwMsgType* e un puntatore a [**CMSG \_ informazioni di \_ codifica \_ firmate**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) per *pvMsgEncodeInfo* per ottenere un handle per il messaggio aperto.
8.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando l'handle recuperato nel passaggio 7 e un puntatore ai dati che devono essere firmati e codificati. Questa funzione può essere chiamata il numero di volte necessario per completare il processo di codifica.
9.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 7 e i tipi di parametro appropriati per accedere ai dati codificati desiderati. Ad esempio, passare CMSG \_ Content \_ param per ottenere un puntatore all'intero messaggio [*PKCS \# 7*](../secgloss/p-gly.md) .

    Se il risultato di questa codifica deve essere usato come [*dati interni*](../secgloss/i-gly.md) per un altro messaggio codificato, ad esempio un messaggio in busta, è \_ \_ necessario passare il parametro CMSG bare Content \_ param. Per un esempio che illustra questo problema, vedere [codice alternativo per la codifica di un messaggio in busta](alternate-code-for-encoding-an-enveloped-message.md)digitale.

10. Chiudere il messaggio chiamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Il risultato di questa procedura è un messaggio codificato che contiene i dati originali, l'hash crittografato dei dati (firma) e le informazioni sul firmatario. È anche presente un puntatore al BLOB codificato desiderato.

Per informazioni sul codice C, vedere [esempio di programma c: firma, codifica, decodifica e verifica di un messaggio](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
