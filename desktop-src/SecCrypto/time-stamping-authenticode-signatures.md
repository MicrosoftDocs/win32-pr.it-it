---
description: L'indicatore di tempo Authenticode è basato su controfirme standard PKCS \# 9. Gli strumenti di firma di Microsoft consentono agli sviluppatori di apporre timestamp contemporaneamente all'aggiunta di firme Authenticode.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Timestamp delle firme Authenticode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3631d402da56d4078cecce65075c92dff0ec7e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231702"
---
# <a name="time-stamping-authenticode-signatures"></a>Timestamp delle firme Authenticode

Le firme Microsoft Authenticode forniscono garanzie di autore e integrità per i dati binari. L'indicatore di tempo Authenticode è basato su controfirme standard PKCS \# 9. Gli strumenti di firma di Microsoft consentono agli sviluppatori di apporre timestamp contemporaneamente all'aggiunta di firme Authenticode. Il timestamp consente di verificare le firme Authenticode anche dopo che i certificati utilizzati per la firma sono scaduti.

## <a name="a-brief-introduction-to-authenticode"></a>Una breve introduzione a Authenticode

[*Authenticode*](../secgloss/a-gly.md) applica la tecnologia di firma digitale per garantire la creazione e l'integrità dei dati binari, ad esempio il software installabile. Un Web browser client o altri componenti di sistema possono utilizzare le firme Authenticode per verificare l'integrità dei dati durante il download o l'installazione del software. Le firme Authenticode possono essere utilizzate con molti formati software, tra cui CAB, exe, ocx e dll.

Microsoft gestisce un elenco di [*autorità di certificazione*](/security/trusted-root/participants-list) pubbliche (CAS). Le autorità emittenti dei certificati Authenticode attualmente includono [SSL.com](https://www.ssl.com/), [DigiCert](https://www.digicert.com/), [Sectigo (comodo)](https://www.sectigo.com/)e [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Informazioni sul timestamp crittografico

In passato, è stata proposta una serie di metodi di timestamp crittografici. Vedere, ad esempio, Haber e Stornetta "How to Time-Stamp a Digital Document" nel *Journal of crittografia* (1991) e Benaloh and de mare "unidirezionale accumulatori: un'alternativa decentralizzata alle firme digitali" nelle note della *lezione Springer-Verlag in computer Science* Vol. 765 (l'Eurocrypt '93). Un abstract esteso di questo articolo è disponibile in [Microsoft Research](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a). Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche. Dato che Time è un valore fisico, anziché una quantità matematica, questi metodi in genere riguardano come collegare gli oggetti in modo che sia possibile determinare l'ordine di creazione o come raggruppare in modo efficiente gli oggetti che possono essere descritti come creati simultaneamente.

I sistemi che prevedono di autenticare il tempo come quantità richiedono sempre una forma di attendibilità. In un'impostazione fortemente contraddittoria, è possibile usare protocolli complessi per garantire un certo grado di sincronizzazione. Tuttavia, questi protocolli richiedono un'interazione approfondita tra le parti interessate. In pratica, se è necessaria solo la certificazione del tempo da una fonte attendibile, l'origine può semplicemente fungere da notatore fornendo un'istruzione firmata (certificazione) che l'oggetto è stato presentato per la firma all'ora indicata.

Il metodo controfirma del timestamp implementato di seguito consente la verifica delle firme anche dopo che il certificato di firma è scaduto o è stato revocato. Il timestamp consente al Verifier di verificare in modo affidabile il tempo in cui la firma è stata approvata e quindi considerare attendibile la firma se fosse valida in quel momento. L'indicatore di data e ora deve avere un'origine ora affidabile e protetta.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>\#Documenti firmati PKCS 7 e controfirme

PKCS \# 7 è un formato standard per i dati crittografici, inclusi i dati firmati, i certificati e gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL). Il \# tipo di interesse PKCS 7 specifico nel contesto del timestamp è costituito dai dati firmati, corrispondenti al \# tipo di contenuto [**SignedData**](signeddata.md) definito PKCS 7.

Il \# pacchetto PKCS 7 è costituito da [**SignedData**](signeddata.md) che identificano il contenuto effettivo e determinate informazioni sui blocchi di firma it e SignerInfo. Un SignerInfo può contenere un controfirma, che in modo ricorsivo è un altro SignerInfo. In linea di principio, potrebbe essere presente una sequenza di tali controfirme. Controfirma è un attributo non autenticato rispetto alla firma in SignerInfo; ovvero, può essere affisso successivamente alla firma originale. Nel formato struttura:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Versione (di PKCS \# 7, in genere versione 1)
-   DigestAlgorithms (raccolta di tutti gli algoritmi usati dai blocchi di firma SignerInfo per l'elaborazione ottimizzata)
-   ContentInfo (contentType Equals [**SignedData**](signeddata.md), più contenuto o riferimento al contenuto)
-   Certificati FACOLTATIVi (raccolta di tutti i certificati usati)
-   CRL FACOLTATIVi (raccolta di tutti i CRL)
-   SignerInfo firme Blocks (la firma effettiva, composta da uno o più blocchi di firma SignerInfo)

SignerInfo (blocco della firma)

-   Versione (di PKCS \# 7, in genere versione 1)
-   Certificato (emittente e numero di serie per identificare in modo univoco il certificato del firmatario in [**SignedData**](signeddata.md))
-   DigestAlgorithm più DigestEncryptionAlgorithm più il digest (hash), più EncryptedDigest (firma effettiva)
-   AuthenticatedAttributes facoltativo (ad esempio, firmato da questo firmatario)
-   UnauthenticatedAttributes facoltativo (ad esempio, non firmato da questo firmatario)

Un esempio di attributo autenticato è l'ora di firma (OID 1.2.840.113549.1.9.5) perché fa parte del servizio timestamp Sign. Un esempio di attributo non autenticato è controfirma (OID 1.2.840.113549.1.9.6) perché può essere affisso dopo la firma. In questo caso, SignerInfo contiene SignerInfo (controfirma).

> [!Note]  
> L'oggetto firmato in controfirma è la firma originale, ovvero il EncryptedDigest del SignerInfo originale.

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool e il processo Authenticode

[SignTool](signtool.md) è disponibile per la firma Authenticode e i dati binari timestamp. Lo strumento viene installato nella \\ cartella bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).

La firma e il timestamp dei dati binari sono relativamente semplici con [SignTool](signtool.md). Il server di pubblicazione deve ottenere un certificato di firma codice da un'autorità di certificazione per la firma di codice commerciale. Per praticità, Microsoft pubblica e aggiorna un elenco di autorità di certificazione pubbliche, incluse quelle che emettono certificati Authenticode. Quando si è pronti per la pubblicazione, i file oggetto vengono firmati e l'ora viene timbrata usando i parametri della riga di comando appropriati con lo strumento SignTool. Il risultato di qualsiasi operazione SignTool è sempre un \# formato PKCS 7 [**SignedData**](signeddata.md).

SignTool accetta come input i dati binari non elaborati che devono essere firmati e con timestamp oppure i dati binari firmati in precedenza per essere contrassegnati come timestamp. I dati precedentemente firmati possono essere contrassegnati con il timestamp del comando **SignTool** .



| Argomento             | Descrizione                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/T** *HTTPAddress* | Indica che il file deve essere contrassegnato come timestamp. È necessario fornire un URL che specifichi l'indirizzo di un server di timestamp. **/t** può essere usato con i comandi di **firma SignTool** e **timestamp di SignTool** . |



 

Per ulteriori informazioni sugli strumenti che possono essere utili in questo contesto, vedere [strumenti di crittografia](cryptography-tools.md) e [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Dettagli di implementazione e formato wire

[SignTool](signtool.md) si basa sull'implementazione di Windows Authenticode per creare e firmare timestamp. [*Authenticode*](../secgloss/a-gly.md) opera su file binari, ad esempio CAB, exe, dll o ocx. Authenticode crea prima di tutto la firma, producendo un \# [**SignedData**](signeddata.md)PKCS 7. Si tratta di un **SignedData** che deve essere controfirmato, come descritto in PKCS \# 9.

Il processo controfirma si verifica in quattro passaggi:

1.  Copiare la firma, ovvero encryptedDigest, dal SignerInfo di PKCS \# 7 [**SignedData**](signeddata.md).
2.  Costruire una richiesta di timestamp il cui contenuto è la firma originale. Inviarlo a Time Stamp server [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) codificato come TimeStampRequest.
3.  Ricevere un timestamp, formattato come secondo PKCS \# 7 [**SignedData**](signeddata.md), restituito dal server di timestamp.
4.  Copiare il SignerInfo dal timestamp direttamente nel \# [**SignedData**](signeddata.md)PKCS 7 originale, come \# controfirma PKCS 9 (ovvero un attributo non autenticato nell'SignerInfo dell'originale).

## <a name="time-stamp-request"></a>Richiesta timestamp

La richiesta di timestamp viene inviata in un messaggio HTTP 1,1 POST. Nell'intestazione HTTP la direttiva CacheControl è impostata su No-cache e la direttiva Content-Type è impostata su Application/ottetto-Stream. Il corpo del messaggio HTTP è una codifica Base64 della codifica [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) della richiesta timestamp.

Sebbene non sia attualmente in uso, la direttiva content-length deve essere utilizzata anche per costruire il messaggio HTTP in quanto consente al server timestamp di individuare la posizione in cui la richiesta si trova all'interno di HTTP POST.

Potrebbero essere presenti anche altre intestazioni HTTP che devono essere ignorate se non sono riconosciute dal richiedente o dal server timestamp.

La richiesta timestamp è un messaggio con codifica ASN. 1. Il formato della richiesta è il seguente.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

CountersignatureType è l' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) che identifica questo come timestamp controfirma e deve essere l'OID esatto 1.3.6.1.4.1.311.3.2.1.

Nessun attributo attualmente incluso nella richiesta timestamp.

Il contenuto è un oggetto ContentInfo come definito da PKCS \# 7. Il contenuto è costituito dai dati da firmare. Per il timestamp della firma, ContentType deve essere costituito da dati e il contenuto deve essere encryptedDigest (Signature) da SignerInfo del \# contenuto PKCS 7 per avere il timestamp.

## <a name="time-stamp-response"></a>Risposta timestamp

La risposta timestamp viene inviata anche all'interno di un messaggio HTTP 1,1. Nell'intestazione HTTP la direttiva Content-Type viene anche impostata su Application/ottetto-Stream. Il corpo del messaggio HTTP è una codifica Base64 della codifica DER della risposta timestamp.

La risposta timestamp è un \# messaggio firmato PKCS 7 firmato dal timestamp. Il ContentInfo del messaggio PKCS \# 7 è identico a ContentInfo ricevuto nel timestamp. Il \# contenuto PKCS 7 contiene l'attributo dell'ora di firma autenticato (definito in PKCS \# 99, OID 1.2.840.113549.9.5).

Quando Authenticode riceve il timestamp dal server, Authenticode incorpora il timestamp nel \# [**SignedData**](signeddata.md) PKCS 7 originale come controfirma. A tale scopo, l'oggetto ContentInfo del SignedData PKCS \# 7  restituito viene eliminato e il SignerInfo del timestamp restituito viene copiato come controfirma in SIGNERINFO dell'originale PKCS \# 7 **SignedData**. La catena di certificati del timestamp viene inoltre copiata nei certificati della SignedData PKCS 7 originale \# come  attributo non autenticato del firmatario originale.

Per ulteriori informazioni su PKCS e altri argomenti relativi alla sicurezza, vedere la [raccolta contenuto del sito Web RSA](https://www.rsa.com/content_library.aspx).

 

 
