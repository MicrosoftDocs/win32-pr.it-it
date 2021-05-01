---
description: Il timestamp Authenticode è basato su controfirma standard PKCS \# 7. Gli strumenti di firma di Microsoft consentono agli sviluppatori di apporre timestamp contemporaneamente all'applicazione delle firme Authenticode.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Timestamp delle firme Authenticode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0232853441d2c11d331c175ac7e8dfd120b341ff
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327186"
---
# <a name="time-stamping-authenticode-signatures"></a>Timestamp delle firme Authenticode

Le firme Microsoft Authenticode forniscono garanzie di autorizzazione e integrità per i dati binari. Il timestamp Authenticode si basa sulle controfirma standard PKCS \# 7. Gli strumenti di firma di Microsoft consentono agli sviluppatori di apporre timestamp contemporaneamente all'applicazione delle firme Authenticode. Il timestamp consente la verifica delle firme Authenticode anche dopo la scadenza dei certificati usati per la firma.

## <a name="a-brief-introduction-to-authenticode"></a>Breve introduzione a Authenticode

[*Authenticode applica*](../secgloss/a-gly.md) la tecnologia di firma digitale per garantire l'autore e l'integrità dei dati binari, ad esempio software installabile. Un Web browser client o altri componenti di sistema possono usare le firme Authenticode per verificare l'integrità dei dati quando il software viene scaricato o installato. Le firme Authenticode possono essere usate con molti formati software, tra cui cab, exe, ocx e dll.

Microsoft gestisce un elenco di autorità [*di*](/security/trusted-root/participants-list) certificazione (CA) pubbliche. Le autorità di certificazione dei certificati Authenticode attualmente [includono SSL.com](https://www.ssl.com/), [Digicert](https://www.digicert.com/), [Sectigo(Comodo)](https://www.sectigo.com/)e [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Informazioni sull'timestamp crittografico

In passato sono stati proposti diversi metodi di timestamp crittografici. Vedere, ad esempio, Haber e Stornetta "Come Time-Stamp un documento digitale" nel *Journal of Cryptology* (1991) e Benaloh e de Mare "One-Way Accumulators: A Decentralized Alternative to Digital Signatures" in *Springer-Verlag Lecture Notes in Computer Science* vol. 765 (EUROCRYPT '93). Un astratto esteso di questo articolo è disponibile in [Microsoft Research.](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a) Queste risorse potrebbero non essere disponibili in alcune lingue, paesi o aree geografiche. Poiché il tempo è una quantità fisica, anziché matematica, questi metodi in genere riguardano come collegare gli oggetti in modo che sia possibile determinarne l'ordine di creazione o come raggruppare in modo efficiente gli oggetti che possono essere tutti descritti come creati contemporaneamente.

I sistemi che richiedono l'autenticazione del tempo come quantità richiedono sempre una qualche forma di attendibilità. In un'impostazione fortemente antagonismo, è possibile usare protocolli complessi per garantire un certo grado di sincronizzazione. Tuttavia, questi protocolli richiedono un'interazione estesa tra le parti interessate. In pratica, se è richiesta solo la certificazione del tempo da un'origine attendibile, l'origine può fungere semplicemente da notario fornendo un'istruzione firmata (certificazione) che indica che l'oggetto è stato presentato per la firma all'ora indicata.

Il metodo di controfirma di timestamp implementato di seguito consente di verificare le firme anche dopo che il certificato di firma è scaduto o è stato revocato. Il timestamp consente al verificatore di conoscere in modo affidabile l'ora in cui la firma è stata affissa e quindi considera attendibile la firma se era valida in quel momento. L'indicatore di data e ora deve avere un'origine ora affidabile e protetta.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>Documenti e controfirma pkcs \# 7 firmati

PKCS 7 è un formato standard per i dati crittografici, inclusi i dati firmati, i certificati e gli elenchi \# di [*revoche*](../secgloss/c-gly.md) di certificati (CRL). Il particolare tipo di interesse PKCS 7 nel contesto del timestamp è dato da dati firmati, corrispondenti al tipo di contenuto \# SignedData definito da PKCS \# 7. [](signeddata.md)

Il pacchetto PKCS 7 è costituito da SignedData che identifica il contenuto effettivo e alcune informazioni su di esso e \# i blocchi di firma SignerInfo. [](signeddata.md) Un SignerInfo può contenere una controfirma, che in modo ricorsivo è un altro SignerInfo. In linea di principio, può essere presente una sequenza di tali controfirma. La controfirma è un attributo non autenticato rispetto alla firma in SignerInfo. ciò significa che può essere apposta successivamente alla firma originale. Sotto forma di struttura:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Versione (pkcs \# 7, in genere versione 1)
-   DigestAlgorithms (raccolta di tutti gli algoritmi usati dai blocchi di firma SignerInfo, per l'elaborazione ottimizzata)
-   ContentInfo (contentType è uguale a [**SignedData,**](signeddata.md)oltre al contenuto o al riferimento al contenuto)
-   CERTIFICATI FACOLTATIVI (raccolta di tutti i certificati usati)
-   CRL FACOLTATIVI (raccolta di tutti i CRL)
-   Blocchi di firma SignerInfo (la firma effettiva, composta da uno o più blocchi di firma SignerInfo)

SignerInfo (blocco di firma)

-   Versione (pkcs \# 7, in genere versione 1)
-   Certificato (autorità emittente e numero di serie per identificare in modo univoco il certificato del firmatario in [**SignedData)**](signeddata.md)
-   DigestAlgorithm più DigestEncryptionAlgorithm più digest (hash), più EncryptedDigest (firma effettiva)
-   OPTIONAL AuthenticatedAttributes (ad esempio, firmato da questo firmatario)
-   OPTIONAL UnauthenticatedAttributes (ad esempio, non firmato da questo firmatario)

Un esempio di attributo autenticato è l'ora di firma (OID 1.2.840.113549.1.9.5) perché fa parte di ciò che il servizio timestamp firma. Un esempio di attributo non autenticato è la controfirma (OID 1.2.840.113549.1.9.6) perché può essere apposta dopo la firma. In questo caso, SignerInfo contiene un SignerInfo (controfirma).

> [!Note]  
> L'oggetto firmato nella controfirma è la firma originale, ovvero EncryptedDigest dell'oggetto SignerInfo originale.

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool e processo Authenticode

[SignTool è](signtool.md) disponibile per la firma Authenticode e l'applicazione di timestamp ai dati binari. Lo strumento viene installato nella cartella Bin del percorso di \\ installazione di Microsoft Windows Software Development Kit (Windows SDK) (SDK).

La firma e l'applicazione di timestamp ai dati binari sono relativamente semplici tramite [SignTool.](signtool.md) L'editore deve ottenere un certificato di firma del codice da una CA per la firma di codice commerciale. Per praticità, Microsoft pubblica e aggiorna un elenco di CA pubbliche, incluse quelle che emettere certificati Authenticode. Quando si è pronti per la pubblicazione, i file oggetto vengono firmati e con timestamp usando i parametri della riga di comando appropriati con lo strumento SignTool. Il risultato di qualsiasi operazione SignTool è sempre un formato PKCS \# 7 [**SignedData.**](signeddata.md)

SignTool accetta come input i dati binari non elaborati da firmare e con timestamp oppure i dati binari firmati in precedenza da inserire nel timestamp. I dati firmati in precedenza possono essere contrassegnati con un timestamp usando il **comando signtool timestamp.**



| Argomento             | Descrizione                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/t** *HTTPAddress* | Indica che il file deve essere contrassegnato con un timestamp. È necessario specificare un URL che specifica l'indirizzo di un server di timestamp. **/t può** essere usato con i **comandi signtool sign e** **signtool timestamp.** |



 

Per altre informazioni sugli strumenti che possono essere utili in questo contesto, vedere [Strumenti di crittografia](cryptography-tools.md) e [SignTool.](signtool.md)

## <a name="implementation-details-and-wire-format"></a>Dettagli di implementazione e formato wire

[SignTool](signtool.md) si basa sull'implementazione di Windows Authenticode per creare firme e timestamp. [*Authenticode*](../secgloss/a-gly.md) opera su file binari, ad esempio cab, exe, dll o ocx. Authenticode crea prima la firma, producendo un \# [**signedData**](signeddata.md)PKCS 7. È questo **SignedData che** deve essere controfirmato, come descritto in PKCS \# 9.

Il processo di controfirma si svolge in quattro passaggi:

1.  Copiare la firma ( ovvero encryptedDigest) da SignerInfo di PKCS \# 7 [**SignedData**](signeddata.md).
2.  Costruire una richiesta timestamp il cui contenuto è la firma originale. Inviarlo al server di timestamp [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) codificato come TimeStampRequest.
3.  Ricevere un timestamp, formattato come secondo PKCS \# 7 [**SignedData,**](signeddata.md)restituito dal server di timestamp.
4.  Copiare SignerInfo dal timestamp direttamente nell'oggetto SignedData PKCS 7 originale \# come controfirma PKCS 9, ovvero un attributo non autenticato nel [](signeddata.md) \# SignerInfo dell'originale.

## <a name="time-stamp-request"></a>Richiesta timestamp

La richiesta timestamp viene inviata all'interno di un messaggio POST HTTP 1.1. Nell'intestazione HTTP la direttiva CacheControl è impostata su no-cache e la direttiva Content-Type è impostata su application/octet-stream. Il corpo del messaggio HTTP è una codifica base64 [*della codifica Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) della richiesta di timestamp.

Sebbene non sia attualmente usata, la direttiva Content-Length deve essere usata anche per costruire il messaggio HTTP perché consente al server di timestamp di individuare la posizione della richiesta all'interno di HTTP POST.

Possono essere presenti anche altre intestazioni HTTP e devono essere ignorate se non sono comprese dal richiedente o dal server di timestamp.

La richiesta di timestamp è un messaggio con codifica ASN.1. Il formato della richiesta è il seguente.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

CountersignatureType è [](../secgloss/o-gly.md) l'identificatore di oggetto (OID) che identifica l'oggetto come controfirma di timestamp e deve essere l'OID esatto 1.3.6.1.4.1.311.3.2.1.

Nessun attributo è attualmente incluso nella richiesta di timestamp.

Il contenuto è un contentInfo come definito da PKCS \# 7. Il contenuto è i dati da firmare. Per il timestamp della firma, ContentType deve essere Data e il contenuto deve essere encryptedDigest (firma) dal SignerInfo del contenuto PKCS 7 da impostare come \# timestamp.

## <a name="time-stamp-response"></a>Risposta timestamp

La risposta del timestamp viene inviata anche all'interno di un messaggio HTTP 1.1. Nell'intestazione HTTP la direttiva Content-Type è impostata anche su application/octet-stream. Il corpo del messaggio HTTP è una codifica base64 della codifica DER della risposta del timestamp.

La risposta del timestamp è un messaggio firmato PKCS \# 7 firmato dall'indicatore di data e ora. L'oggetto ContentInfo del messaggio PKCS \# 7 è identico all'oggetto ContentInfo ricevuto nel timestamp. Il contenuto PKCS 7 contiene l'attributo autenticato dell'ora di firma \# (definito in PKCS \# 99, OID 1.2.840.113549.9.5).

Dopo che Authenticode ha ricevuto il timestamp dal server, lo incorpora nell'oggetto SignedData PKCS 7 originale come \# controfirma. [](signeddata.md) A tale scopo, l'oggetto ContentInfo dell'oggetto SignedData PKCS 7 restituito viene eliminato e l'oggetto SignerInfo del timestamp restituito viene copiato come controfirma nel SignerInfo dell'oggetto \# SignedData PKCS  \# 7 **originale.** La catena di certificati dell'indicatore di data e ora viene copiata anche in Certificati nell'oggetto SignedData PKCS 7 originale come attributo non autenticato del \# firmatario originale. 

Per altre informazioni su PKCS e altri argomenti relativi alla sicurezza, vedere la [raccolta contenuto del sito Web RSA](https://www.rsa.com/content_library.aspx).

 

 
