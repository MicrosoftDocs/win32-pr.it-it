---
description: Convalida della catena di certificati
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Convalida della catena di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436513ae9199feb7ba5fcba399537da198ba85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232284"
---
# <a name="validating-the-certificate-chain"></a>Convalida della catena di certificati

In questo argomento viene descritto come convalidare la catena di certificati del driver quando si utilizza COPP (Certified Output Protocol).

La catena di certificati del driver grafico è un documento XML. La catena di certificati contiene tre certificati. Il primo certificato è denominato *certificato foglia* e è il certificato Copp del driver. Il certificato successivo è il certificato di firma del fornitore dell'hardware indipendente (IHV). L'ultimo certificato è il certificato di firma di Microsoft. Per assicurarsi che il driver di grafica sia un dispositivo COPP legittimo, l'applicazione deve convalidare tutti e tre questi certificati. Un programma dannoso può impedire il funzionamento di COPP se un'applicazione non convalida correttamente i certificati nella catena.

Le catene di certificati COPP utilizzano il set di caratteri UTF-8. I dati binari nei certificati, ad esempio la chiave pubblica RSA, sono codificati in base 64 e archiviati in ordine big endian. (*Big-Endian* significa che il byte più significativo viene archiviato nella posizione di memoria con l'indirizzo più basso).

Alcuni elementi all'interno di un certificato contengono valori booleani per indicare che esiste una funzionalità del certificato. Se la funzionalità esiste, il valore dell'elemento figlio corrispondente viene impostato su 1. Se una funzionalità non è presente, l'elemento figlio non è presente nel certificato.

### <a name="xml-element-definitions"></a>Definizioni degli elementi XML

Di seguito sono riportate le definizioni degli elementi nello schema del certificato:

-   **Certificate**. Elemento radice del documento XML. Contiene gli elementi del certificato, uno per ogni certificato nella catena.
-   **Certificato**. Contiene un certificato. Questo elemento contiene i dati e gli elementi della firma.
-   **Dati**. Contiene informazioni sul certificato. In particolare, contiene la chiave pubblica del certificato e il tipo. L'elemento dati contiene gli elementi figlio seguenti:
    -   **PublicKey**. Contiene la chiave pubblica RSA del certificato. L'elemento PublicKey contiene un elemento di un valore di valore che contiene un elemento RSAKeyValue. L'elemento RSAKeyValue ha due elementi figlio, modulo ed esponente, che definiscono la chiave pubblica. Gli elementi modulo ed esponente sono codificati in base 64 e archiviati in ordine big endian.
    -   **Utilizzo di dati**. Se il certificato è il certificato COPP del driver, questo elemento deve contenere un elemento figlio denominato EncryptKey. Se il certificato è il certificato di firma di IHV o il certificato di firma di Microsoft, deve contenere un elemento figlio denominato SignCertificate. Entrambi questi elementi figlio contengono valori booleani.
    -   **SecurityLevel**. Questo elemento deve essere ignorato.
    -   **ManufacturerData**. Specifica il produttore e il modello del dispositivo di grafica. Questo elemento è solo informativo.
    -   **Features**. Contiene gli elementi figlio che specificano l'utilizzo del certificato. L'unico elemento pertinente per COPP è l'elemento COPPCertificate. Potrebbero essere presenti altri elementi figlio; in tal caso, devono essere ignorati. Se l'elemento COPPCertificate esiste, il certificato è un certificato COPP. Questo elemento deve essere presente nel nodo foglia di un certificato COPP valido. Questo elemento contiene un valore booleano.
-   **Firma**. Contiene la firma per il certificato. Contiene gli elementi figlio seguenti:
    -   **SignedInfo**. Contiene informazioni sulla firma. L'elemento figlio importante di questo elemento è l'elemento DigestValue, che contiene il valore con codifica Base64 dell'hash SHA-1 sull'elemento dati. Il valore digest viene utilizzato per controllare il certificato rispetto all'elenco di revoche di certificati (CRL).
    -   **SignatureValue**. Questo valore viene calcolato sull'elemento dati e viene calcolato in base allo schema di firma digitale RSASSA-PSS definito in Public-Key Cryptography Standards (PKCS) \# 1 (versione 2,1). Per informazioni su PKCS \# 1, visitare [https://www.rsa.com/](https://www.rsa.com/) .
    -   **Informazioni sui dati**. Contiene la chiave pubblica RSA del certificato successivo nella catena. Questo elemento viene utilizzato per verificare che i dati nell'elemento dati non siano stati manomessi. Questo elemento ha lo stesso formato dell'elemento PublicKey.

### <a name="certificate-validation"></a>Convalida del certificato

Per convalidare correttamente la catena di certificati, l'applicazione deve eseguire i passaggi seguenti. Se un passaggio ha esito negativo o se un elemento a cui si fa riferimento in queste procedure non esiste, la convalida ha esito negativo.

### <a name="validate-certificate-collection-procedure"></a>Procedura convalida raccolta certificati

Per convalidare la catena di certificati, seguire questa procedura:

1.  Verificare che il formato di certificate sia XML.
2.  Verificare che l'oggetto certificate sia codificato in formato UTF-8.
3.  Verificare che l'attributo Version nell'elemento certificate sia 2,0 o versione successiva.
4.  Verificare che la catena di certificati contenga esattamente tre elementi del certificato.
5.  Scorrere ogni elemento del certificato nella catena di certificati ed eseguire la procedura di convalida del certificato, descritta di seguito, su ciascuno di essi.

### <a name="validate-certificate-procedure"></a>Procedura di convalida del certificato

Per convalidare un certificato nella catena, seguire questa procedura:

1.  Verificare che nessuno degli elementi figlio nell'elemento dati sia duplicato. Ad esempio, deve essere presente un solo elemento PublicKey.
2.  Verificare che l'elemento data/PublicKey/valore di RSAKeyValue/modulo esista. Il valore con decodifica Base64 deve avere una lunghezza di 256 byte per tutti i certificati ad eccezione della radice. Nel certificato radice, questo elemento deve essere lungo 128 byte.
3.  Verificare che l'elemento data/PublicKey/valore di RSAKeyValue/esponente esista. Il valore con decodifica Base64 non deve essere maggiore di 4 byte.
4.  Se il certificato è il certificato foglia, verificare quanto segue:
    -   L'elemento DataUsage contiene un elemento EncryptKey con il valore 1.
    -   L'elemento features contiene un elemento COPPCertificate con il valore 1.
5.  Se il certificato non è il certificato foglia, verificare quanto segue:
    -   Il modulo e l'esponente dell'elemento data/PublicKey corrispondono esattamente al modulo e all'esponente dell'elemento Signature/datainfo del certificato precedente.
    -   L'elemento DataUsage contiene un elemento SignCertificate con il valore 1.
6.  Utilizzare l'algoritmo hash SHA-1 per eseguire l'hashing di ogni byte nell'elemento dati del certificato. È necessario eseguire l'hashing di ogni byte dal primo carattere del <Data> tag all'ultimo carattere </Data> del tag di chiusura. Il valore hash viene utilizzato per verificare il certificato rispetto all'elenco di revoche di certificati (CRL), come descritto in [elenchi di revoche di certificati](certificate-revocation-lists.md)
7.  Confrontare il valore hash del passaggio 6 con il valore decodificato in base 64 dell'elemento Signature/SignedInfo/reference/DigestValue. Questi valori devono corrispondere.
8.  Eseguire la procedura Verify Signature, descritta di seguito.
9.  Se questo certificato non è il certificato finale della catena, salvare il valore Signature/Keychain/valore/RSAKeyValue per l'iterazione successiva del ciclo.
10. Se questo certificato è il certificato finale della catena, verificare che il valore di Signature/Key Info/chiave/valore/RSAKeyValue corrisponda alla chiave pubblica di Microsoft. La chiave pubblica Microsoft presenta i seguenti valori con codifica Base64:
    -   Modulo

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Esponente `AQAB`

### <a name="verify-signature-procedure"></a>Verificare la procedura di firma

Il valore dell'elemento SignatureValue viene calcolato sull'elemento dati in base allo schema di firma digitale RSASSA-PSS definito in PKCS \# 1 versione 2,1 (in seguito denominato Pkcs). Per verificare la firma, seguire questa procedura:

1.  Decodificare i valori del modulo e dell'esponente nell'elemento Signature/info/RSAKeyValue/valore dell'elemento. Questi valori definiscono la chiave pubblica RSA del certificato di firma.
2.  Decodificare l'elemento Signature/SignatureValue.
3.  Calcolare l'operazione RSASSA-PSS-Verify, definita nella sezione 8.1.2 di PKCS.

Per l'operazione RSASSA-PSS-Verify, usare gli input seguenti:

-   (*n*,*e*) è la chiave pubblica del passaggio 1.
-   *M* è costituito da tutti i byte nell'elemento dati, inclusi i tag <Data> e</Data> che racchiudono l'elemento.
-   *S* è il valore della firma decodificato dal passaggio 2.

L'operazione RSASSA-PSS-Verify usa l'operazione EMSA-PSS-ENCODE, definita nella sezione 9.1.1. di PKCS. Per questa operazione, COPP usa le opzioni seguenti:

-   Hash = SHA-1
-   *hlen* = 20
-   MGF (funzione di generazione della maschera) = maschera MGF1
-   *slen* = 0

La funzione di generazione della maschera maschera MGF1 è definita nell'Appendice B. 2 di PKCS. Per questa funzione, COPP usa le opzioni seguenti:

-   Hash = SHA-1
-   *hlen* = 20

L'output dell'operazione RSASSA-PSS-Verify indica se la firma è valida o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



