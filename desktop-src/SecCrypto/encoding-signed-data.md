---
description: Illustra la procedura per la codifica di un messaggio firmato.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codifica dei dati firmati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e5c3ab338c4e7b251416f1a488747eb0c9b897c1fa02082afcb580cb12341b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874846"
---
# <a name="encoding-signed-data"></a>Codifica dei dati firmati

[*I dati*](../secgloss/s-gly.md) firmati sono costituiti da contenuto di qualsiasi tipo e [*hash*](../secgloss/h-gly.md) di messaggi crittografati del contenuto di zero o più firmatari. L'hash risultante può confermare che il messaggio originale non è stato modificato dopo la firma e che determinate persone o entità hanno firmato i dati.

Nella figura seguente viene illustrata la procedura per la codifica di un messaggio firmato. L'elenco seguente illustra i passaggi.

Un messaggio può avere più firmatari, algoritmi hash e certificati. Mentre l'illustrazione mostra solo i certificati, [*i CRL*](../secgloss/c-gly.md)e [*gli CCL*](../secgloss/c-gly.md) possono usare lo stesso processo. Si adattano all'illustrazione in qualsiasi posizione in cui vengono visualizzati i certificati.

![codifica di un messaggio firmato](images/signmsg2.png)

Il processo generale per la codifica [*dei dati firmati*](../secgloss/s-gly.md) è il seguente.

**Per codificare i dati firmati**

1.  I dati vengono creati (se necessario) e viene recuperato un puntatore a esso.
2.  Viene [*aperto un*](../secgloss/c-gly.md) archivio certificati contenente il certificato del firmatario.
3.  Viene recuperata la chiave privata per il certificato. Esistono due proprietà che devono essere impostate sul certificato prima di usarlo. Uno viene usato per associare un certificato a un CSP specifico e, all'interno di tale CSP, a un contenitore di [*chiavi private specifico.*](../secgloss/k-gly.md) L'altro viene usato per indicare quale algoritmo hash deve essere usato quando viene chiamata un'operazione [*hash.*](../secgloss/h-gly.md) Questi devono essere impostati una sola volta.
4.  La proprietà di un certificato determina l'algoritmo hash.
5.  Un hash dei dati viene creato inviando i dati tramite la funzione hash.
6.  La firma viene creata crittografando l'hash usando la chiave privata, ottenuta tramite una proprietà nel certificato.
7.  I dati seguenti sono inclusi nel messaggio firmato completato:
    -   Dati originali da firmare
    -   Algoritmi hash
    -   Firme
    -   Strutture di informazioni sul firmatario, che include l'identificatore del firmatario (autorità emittente del certificato e numero di serie)
    -   Certificati del firmatario (facoltativo)

Questa procedura illustra un caso semplice. I casi più complessi includono attributi autenticati inclusi nel messaggio. Quando il tipo di contenuto è altro che una stringa **BYTE** o è presente almeno un attributo autenticato insieme a qualsiasi tipo di dati, sono necessari due attributi autenticati standard: il tipo di contenuto (dati) e l'hash del contenuto. In questi casi, [*CryptoAPI*](../secgloss/c-gly.md) fornisce automaticamente questi due attributi obbligatori. Le funzioni di messaggi di basso livello eseguono l'hashing degli attributi autenticati, crittografano l'hash con la chiave privata e lo forniscono come firma.

Usare le funzioni di messaggi di basso livello per eseguire le attività appena elencate, usando la procedura seguente.

**Per codificare un messaggio firmato**

1.  Creare o recuperare il contenuto.
2.  Ottenere un provider di crittografia.
3.  Ottenere i certificati del firmatario.
4.  Inizializzare [**la struttura CMSG \_ SIGNER \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info)
5.  Inizializzare la [**struttura CMSG \_ SIGNED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
6.  Chiamare [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) per ottenere le dimensioni del BLOB del messaggio codificato. Allocare memoria.
7.  Chiamare [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), passando CMSG SIGNED per dwMsgType e un puntatore \_ a [**CMSG SIGNED \_ \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) per  *pvMsgEncodeInfo* per ottenere un handle per il messaggio aperto.
8.  Chiamare [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), passando l'handle recuperato nel passaggio 7 e un puntatore ai dati da firmare e codificare. Questa funzione può essere chiamata il numero di volte necessario per completare il processo di codifica.
9.  Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passando l'handle recuperato nel passaggio 7 e i tipi di parametro appropriati per accedere ai dati codificati desiderati. Ad esempio, passare CMSG CONTENT PARAM per ottenere un puntatore \_ \_ all'intero [*messaggio PKCS \# 7.*](../secgloss/p-gly.md)

    Se il risultato di questa codifica [](../secgloss/i-gly.md) deve essere usato come dati interni per un altro messaggio codificato, ad esempio un messaggio con busta, è necessario passare il parametro \_ CMSG BARE \_ CONTENT \_ PARAM. Per un esempio che illustra questa operazione, vedere [Codice alternativo per la codifica di un messaggio in busta](alternate-code-for-encoding-an-enveloped-message.md).

10. Chiudere il messaggio chiamando [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Il risultato di questa procedura è un messaggio codificato che contiene i dati originali, l'hash crittografato di tali dati (firma) e le informazioni sul firmatario. È presente anche un puntatore al BLOB codificato desiderato.

Per informazioni dettagliate sulla codifica C, vedere [Esempio di programma C: firma, codifica,](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)decodifica e verifica di un messaggio .

 

 
