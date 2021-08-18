---
description: CNG fornisce un modello per l'archiviazione con chiave privata che consente di adattarsi alle esigenze attuali e future della creazione di applicazioni che usano funzionalità di crittografia come la crittografia a chiave pubblica o privata, nonché alle richieste di archiviazione del materiale della chiave.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Recupero e Archiviazione chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b2100f005f0ff293e34a3f4c0a7460b7a4d4e9c2b15fbe0b3577b5e52394a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907687"
---
# <a name="key-storage-and-retrieval"></a>Recupero e Archiviazione chiave

-   [Architettura Archiviazione chiave](#key-storage-architecture)
-   [Tipi di chiave](#key-types)
-   [Algoritmi supportati](#supported-algorithms)
-   [Directory e file chiave](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Architettura Archiviazione chiave

CNG fornisce un modello per l'archiviazione con chiave privata che consente di adattarsi alle esigenze attuali e future della creazione di applicazioni che usano funzionalità di crittografia come la crittografia a chiave pubblica o privata, nonché alle richieste di archiviazione del materiale della chiave. Il router di archiviazione delle chiavi è la routine centrale in questo modello e viene implementato in Ncrypt.dll. Un'applicazione accede ai provider di archiviazione chiavi (KSP) nel sistema tramite il router di archiviazione delle chiavi, che nasconde dettagli, ad esempio l'isolamento della chiave, sia dall'applicazione che dal provider di archiviazione stesso. La figura seguente illustra la progettazione e la funzione dell'architettura di isolamento della chiave CNG.

![Provider di archiviazione chiavi cng](images/cng-key-storage-provider.png)

Per soddisfare i requisiti di criteri comuni, le chiavi di lunga durata devono essere isolate in modo che non siano mai presenti nel processo dell'applicazione. CNG attualmente supporta l'archiviazione di chiavi private asimmetriche usando il KSP software Microsoft incluso in Windows Server 2008 e Windows Vista e installato per impostazione predefinita.

L'isolamento delle chiavi è abilitato per impostazione predefinita in Windows Server 2008 e Windows Vista. La funzionalità di isolamento delle chiavi non è disponibile nelle piattaforme precedenti a queste. Inoltre, i KSP di terze parti non vengono caricati nel servizio di isolamento delle chiavi (processo LSA). Nel servizio di isolamento delle chiavi viene caricato solo Microsoft KSP.

Il processo LSA viene usato come processo di isolamento della chiave per ottimizzare le prestazioni. Tutti gli accessi alle chiavi private passano attraverso il router di archiviazione delle chiavi, che espone un set completo di funzioni per la gestione e l'uso delle chiavi private.

CNG archivia la parte pubblica della chiave archiviata separatamente dalla parte privata. La parte pubblica di una coppia di chiavi viene mantenuta anche nel servizio di isolamento delle chiavi ed è accessibile tramite la chiamata di procedura remota locale (LRPC). Il router di archiviazione chiavi usa LRPC durante la chiamata al processo di isolamento della chiave. Tutti gli accessi alle chiavi private passano attraverso il router della chiave privata e vengono controllati da CNG.

Come descritto in precedenza, è possibile supporto di un'ampia gamma di dispositivi di archiviazione hardware. In ogni caso, l'interfaccia per tutti questi dispositivi di archiviazione è identica. Include funzioni per eseguire varie operazioni di chiave privata, nonché funzioni relative all'archiviazione e alla gestione delle chiavi.

CNG fornisce un set di API usate per creare, archiviare e recuperare chiavi crittografiche. Per un elenco di queste API, vedere [Funzioni Archiviazione CNG.](cng-key-storage-functions.md)

## <a name="key-types"></a>Tipi di chiave

CNG supporta i tipi di chiave seguenti:

-   Diffie-Hellman chiavi pubbliche e private.
-   Chiavi pubbliche e private DSA (Digital Signature Algorithm, FIPS 186-2).
-   Chiavi pubbliche e private RSA (PKCS \# 1).
-   Diverse chiavi pubbliche e private (CryptoAPI) legacy.
-   Chiavi pubbliche e private di crittografia a curva ellittica.

## <a name="supported-algorithms"></a>Algoritmi supportati

CNG supporta gli algoritmi di chiave seguenti.

| Algoritmo | Lunghezza chiave/hash (bit)             |
|-----------|------------------------------------|
| RSA       | Da 512 a 16384, in incrementi a 64 bit |
| Dh        | Da 512 a 16384, in incrementi a 64 bit |
| DSA       | Da 512 a 1024, in incrementi a 64 bit  |
| Ecdsa     | P-256, P-384, P-521 (curve NIST)  |
| ECDH      | P-256, P-384, P-521 (curve NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Directory e file chiave

I CSP CryptoAPI legacy Microsoft archiviano le chiavi private nelle directory seguenti.

| Tipo di chiave                | Directory                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Privato dell'utente            | SID utente RSA %APPDATA% \\ Microsoft \\ Crypto \\ \\ \\<br/>%APPDATA% \\ \\ SID utente Microsoft Crypto \\ \\ *DSS*\\<br/>                                                   |
| Sistema locale privato    | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-18\\<br/>%ALLUSERSPROFILE% \\ Dati applicazione Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-18\\<br/>   |
| Servizio locale privato   | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-19\\<br/>%ALLUSERSPROFILE% \\ Dati applicazione Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-19\\<br/>   |
| Servizio di rete privato | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-20\\<br/>%ALLUSERSPROFILE% \\ Dati applicazione Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-20\\<br/>   |
| Privato condiviso          | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto RSA \\ \\ \\ \\ MachineKeys<br/>%ALLUSERSPROFILE% \\ Dati applicazione Microsoft Crypto \\ \\ \\ DSS \\ MachineKeys<br/> |



 

CNG archivia le chiavi private nelle directory seguenti.

| Tipo di chiave                | Directory                                                          |
|-------------------------|--------------------------------------------------------------------|
| Privato dell'utente            | %APPDATA% \\ Chiavi di crittografia \\ \\ Microsoft                                 |
| Sistema locale privato    | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto \\ \\ \\ SystemKeys |
| Servizio locale privato   | %WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Servizio di rete privato | %WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Privato condiviso          | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto \\ \\ \\ Keys       |



 

Di seguito sono riportate alcune delle differenze tra i contenitori di chiavi CryptoAPI e CNG.

-   CNG usa nomi di file diversi per i file di chiave rispetto ai file di chiave creati dal Rsaenh.dll e Dssenh.dll CSP legacy. Anche i file di chiave legacy hanno l'estensione .key, ma i file di chiave CNG non hanno l'estensione .key.
-   CNG supporta completamente i nomi dei contenitori di chiavi Unicode. CNG usa un hash del nome del contenitore Unicode, mentre CryptoAPI usa un hash del nome del contenitore ANSI.
-   CNG è più flessibile per quanto riguarda le coppie di chiavi RSA. CNG, ad esempio, supporta esponenti pubblici di lunghezza superiore a 32 bit e chiavi in cui p e q hanno lunghezze diverse.
-   In CryptoAPI il file del contenitore di chiavi viene archiviato in una directory il cui nome è l'equivalente testuale del SID dell'utente. Questo non è più il caso in CNG, che elimina la difficoltà di spostare gli utenti da un dominio a un altro senza perdere tutte le chiavi private.
-   I nomi di chiave e KSP CNG sono limitati ai caratteri Unicode **MAX \_ PATH.** I nomi di chiave e CSP CryptoAPI sono limitati ai caratteri ANSI **\_ MAX PATH.**
-   CNG offre la funzionalità delle proprietà chiave definite dall'utente. Gli utenti possono creare e associare proprietà personalizzate alle chiavi e archiviarle con chiavi persistenti.

Quando si rende persistente una chiave, CNG può creare due file. Il primo file contiene la chiave privata nel nuovo formato CNG e viene sempre creato. Questo file non è utilizzabile dai CSP CryptoAPI legacy. Il secondo file contiene la stessa chiave privata nel contenitore di chiavi CryptoAPI legacy. Il secondo file è conforme al formato e alla posizione usati da Rsaenh.dll. La creazione del secondo file viene eseguita solo se viene specificato il flag **FLAG NCRYPT \_ WRITE KEY TO LEGACY STORE \_ \_ \_ \_ \_ quando** viene chiamata la funzione [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) per finalizzare una chiave RSA. Questa funzionalità non è supportata per le chiavi DSA e DH.

Quando un'applicazione tenta di aprire una chiave persistente esistente, CNG tenta innanzitutto di aprire il file CNG nativo. Se questo file non esiste, CNG tenta di individuare una chiave corrispondente nel contenitore di chiavi CryptoAPI legacy.

Quando si spostano o copiano chiavi CryptoAPI da un computer di origine a un computer di destinazione con Windows Utilità di migrazione stato utente (USMT), CNG non riuscirà ad accedere alle chiavi nel computer di destinazione. Per accedere a tali chiavi migrate, è necessario usare CryptoAPI.

 

 




