---
description: Convalida della catena di certificati
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Convalida della catena di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c63aab8cca71453aff456f145e8f04affd85b4b1f80aa770cbf589970874f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072135"
---
# <a name="validating-the-certificate-chain"></a>Convalida della catena di certificati

Questo argomento descrive come convalidare la catena di certificati del driver quando si usa il protocollo COPP (Certified Output Protection Protocol).

La catena di certificati del driver grafico è un documento XML. La catena di certificati contiene tre certificati. Il primo certificato è denominato *certificato foglia* ed è il certificato COPP del driver. Il certificato successivo è il certificato di firma del fornitore di hardware indipendente (IHV). L'ultimo certificato è il certificato di firma di Microsoft. Per assicurarsi che il driver di grafica sia un dispositivo COPP legittimo, l'applicazione deve convalidare tutti e tre questi certificati. Un programma dannoso può impedire il funzionamento di COPP se un'applicazione non convalida correttamente i certificati nella catena.

Le catene di certificati COPP usano il set di caratteri UTF-8. I dati binari nei certificati, ad esempio la chiave pubblica RSA, sono codificati in base 64 e archiviati in ordine big-endian. (*Big-endian* indica che il byte più significativo viene archiviato nella posizione di memoria con l'indirizzo più basso.

Alcuni elementi all'interno di un certificato contengono valori booleani per indicare che esiste una funzionalità del certificato. Se la funzionalità esiste, il valore dell'elemento figlio corrispondente viene impostato su 1. Se non è presente una funzionalità, tale elemento figlio non è presente nel certificato.

### <a name="xml-element-definitions"></a>Definizioni di elementi XML

Di seguito sono riportate le definizioni per gli elementi nello schema del certificato:

-   **CertificateCollection**. Elemento radice del documento XML. Contiene gli elementi Certificate, uno per ogni certificato nella catena.
-   **Certificato**. Contiene un certificato. Questo elemento contiene gli elementi Data e Signature.
-   **Dati**. Contiene informazioni sul certificato. In particolare, contiene la chiave pubblica e il tipo del certificato. L'elemento Data contiene gli elementi figlio seguenti:
    -   **PublicKey**. Contiene la chiave pubblica RSA del certificato. L'elemento PublicKey contiene un elemento KeyValue, che contiene un elemento RSAKeyValue. L'elemento RSAKeyValue ha due elementi figlio, Modulus ed Exponent, che definiscono la chiave pubblica. Gli elementi Modulo ed Esponente sono codificati in base 64 e archiviati in ordine big-endian.
    -   **KeyUsage**. Se il certificato è il certificato COPP del driver, questo elemento deve contenere un elemento figlio denominato EncryptKey. Se il certificato è il certificato di firma dell'IHV o il certificato di firma di Microsoft, deve contenere un elemento figlio denominato SignCertificate. Entrambi questi elementi figlio contengono valori booleani.
    -   **SecurityLevel**. Questo elemento deve essere ignorato.
    -   **ManufacturerData**. Specifica il produttore e il modello della periferica grafica. Questo elemento è solo informativo.
    -   **Features**. Contiene elementi figlio che specificano l'utilizzo del certificato. L'unico elemento rilevante per COPP è l'elemento COPPCertificate. Potrebbero essere presenti altri elementi figlio. In tal caso, devono essere ignorati. Se l'elemento COPPCertificate esiste, il certificato è un certificato COPP. Questo elemento deve essere presente nel nodo foglia di un certificato COPP valido. Questo elemento contiene un valore booleano.
-   **Firma**. Contiene la firma per questo certificato. Contiene gli elementi figlio seguenti:
    -   **SignedInfo**. Contiene informazioni sulla firma. L'elemento figlio importante di questo elemento è l'elemento DigestValue, che contiene il valore con codifica Base64 dell'hash SHA-1 sull'elemento Data. Il valore digest viene usato quando si controlla il certificato rispetto all'elenco di revoche di certificati (CRL).
    -   **SignatureValue**. Questo valore viene calcolato sull'elemento Data e viene calcolato in base a uno schema di firma digitale RSASSA-PSS definito in Public-Key Cryptography Standards (PKCS) \# 1 (versione 2.1). Per informazioni su PKCS \# 1, visitare [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Contiene la chiave pubblica RSA del certificato successivo nella catena. Questo elemento viene utilizzato per verificare che i dati nell'elemento Data non siano stati manomissionati. Questo elemento ha lo stesso formato dell'elemento PublicKey.

### <a name="certificate-validation"></a>Convalida del certificato

L'applicazione deve eseguire i passaggi seguenti per convalidare correttamente la catena di certificati. Se un passaggio ha esito negativo o se un elemento a cui si fa riferimento in queste procedure non esiste, la convalida ha esito negativo.

### <a name="validate-certificate-collection-procedure"></a>Convalidare la procedura di raccolta certificati

Per convalidare la catena di certificati, seguire questa procedura:

1.  Verificare che CertificateCollection sia xml ben formato.
2.  Verificare che CertificateCollection sia codificato in formato UTF-8.
3.  Verificare che l'attributo Version nell'elemento CertificateCollection sia 2.0 o versione successiva.
4.  Verificare che la catena di certificati contenga esattamente tre elementi Certificate.
5.  Scorrere ogni elemento Certificato nella catena di certificati ed eseguire la procedura Convalida certificato, descritta di seguito, su ognuno di essi.

### <a name="validate-certificate-procedure"></a>Convalidare la procedura del certificato

Per convalidare un certificato nella catena, seguire questa procedura:

1.  Verificare che nessuno degli elementi figlio nell'elemento Data sia duplicato. Ad esempio, deve essere presente un solo elemento PublicKey.
2.  Assicurarsi che l'elemento Data/PublicKey/KeyValue/RSAKeyValue/Modulus esista. Il valore decodificato in base64 deve essere lungo 256 byte per tutti i certificati ad eccezione della radice. Nel certificato radice questo elemento deve avere una lunghezza di 128 byte.
3.  Assicurarsi che l'elemento Data/PublicKey/KeyValue/RSAKeyValue/Exponent esista. Il valore decodificato in base64 non deve essere maggiore di 4 byte.
4.  Se questo certificato è il certificato foglia, verificare quanto segue:
    -   L'elemento KeyUsage contiene un elemento EncryptKey con valore 1.
    -   L'elemento Features contiene un elemento COPPCertificate con valore 1.
5.  Se questo certificato non è il certificato foglia, verificare quanto segue:
    -   Il modulo e l'esponente dell'elemento Data/PublicKey corrispondono esattamente al modulo e all'esponente dall'elemento Signature/KeyInfo del certificato precedente.
    -   L'elemento KeyUsage contiene un elemento SignCertificate con il valore 1.
6.  Usare l'algoritmo hash SHA-1 per eseguire l'hashing di ogni byte nell'elemento Data del certificato. Per ogni byte dal primo carattere del <Data> tag all'ultimo carattere </Data> del tag di chiusura deve essere eseguito l'hashing. Il valore hash viene usato per verificare il certificato rispetto all'elenco di revoche di certificati (CRL), come descritto in [Elenchi di revoche di certificati](certificate-revocation-lists.md)
7.  Confrontare il valore hash del passaggio 6 con il valore decodificato in base64 dell'elemento Signature/SignedInfo/Reference/DigestValue. Questi valori devono corrispondere.
8.  Eseguire la procedura Verifica firma descritta di seguito.
9.  Se questo certificato non è il certificato finale nella catena, salvare il valore Signature/KeyInfo/KeyValue/RSAKeyValue per l'iterazione successiva del ciclo.
10. Se questo certificato è il certificato finale nella catena, assicurarsi che il valore di Signature/KeyInfo/KeyValue/RSAKeyValue corrisponda alla chiave pubblica di Microsoft. La chiave pubblica Microsoft ha i valori con codifica Base64 seguenti:
    -   Modulo:

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Esponente: `AQAB`

### <a name="verify-signature-procedure"></a>Procedura di verifica della firma

Il valore dell'elemento SignatureValue viene calcolato sull'elemento Data secondo lo schema di firma digitale RSASSA-PSS definito in PKCS \# 1 versione 2.1 (hereinafter detto PKCS). Per verificare questa firma, seguire questa procedura:

1.  Decodificare i valori modulo ed esponente nell'elemento Signature/KeyInfo/KeyValue/RSAKeyValue. Questi valori definiscono la chiave pubblica RSA del certificato di firma.
2.  Decodificare l'elemento Signature/SignatureValue.
3.  Calcolare l'operazione RSASSA-PSS-Verify, definita nella sezione 8.1.2 di PKCS.

Per l'operazione RSASSA-PSS-Verify, usare gli input seguenti:

-   (*n*,*e*) è la chiave pubblica del passaggio 1.
-   *M* è tutti i byte nell'elemento Data, inclusi i <Data> tag e</Data> che racchiudno l'elemento.
-   *S* è il valore della firma decodificata del passaggio 2.

L'operazione RSASSA-PSS-Verify usa l'operazione EMSA-PSS-ENCODE, definita nella sezione 9.1.1. di PKCS. Per questa operazione, COPP usa le opzioni seguenti:

-   Hash = SHA-1
-   *hLen* = 20
-   MGF (funzione di generazione maschera) = MGF1
-   *sLen* = 0

La funzione di generazione della maschera MGF1 è definita nell'appendice B.2 di PKCS. Per questa funzione, COPP usa le opzioni seguenti:

-   Hash = SHA-1
-   *hLen* = 20

L'output dell'operazione RSASSA-PSS-Verify indica se la firma è valida o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del protocollo COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



