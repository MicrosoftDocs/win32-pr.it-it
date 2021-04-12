---
description: CNG fornisce un modello per l'archiviazione delle chiavi private che consente di adattarsi alle esigenze attuali e future della creazione di applicazioni che utilizzano funzionalità di crittografia come la crittografia a chiave pubblica o privata, nonché le richieste di archiviazione del materiale della chiave.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Archiviazione e recupero delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd6319353440c580d53990075a71613a1eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347756"
---
# <a name="key-storage-and-retrieval"></a>Archiviazione e recupero delle chiavi

-   [Architettura di archiviazione chiavi](#key-storage-architecture)
-   [Tipi di chiave](#key-types)
-   [Algoritmi supportati](#supported-algorithms)
-   [Directory e file principali](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Architettura di archiviazione chiavi

CNG fornisce un modello per l'archiviazione delle chiavi private che consente di adattarsi alle esigenze attuali e future della creazione di applicazioni che utilizzano funzionalità di crittografia come la crittografia a chiave pubblica o privata, nonché le richieste di archiviazione del materiale della chiave. Il router di archiviazione chiavi è la routine centrale di questo modello e viene implementato in Ncrypt.dll. Un'applicazione accede ai provider di archiviazione chiavi (KSP) nel sistema tramite il router di archiviazione chiavi, che nasconde i dettagli, ad esempio l'isolamento delle chiavi, sia dall'applicazione che dal provider di archiviazione. Nella figura seguente viene illustrata la progettazione e la funzione dell'architettura di isolamento delle chiavi CNG.

![provider di archiviazione chiavi CNG](images/cng-key-storage-provider.png)

Per conformarsi ai requisiti di criteri comuni (CC), le chiavi di lunga durata devono essere isolate in modo che non siano mai presenti nel processo dell'applicazione. CNG supporta attualmente l'archiviazione di chiavi private asimmetriche usando il provider di archiviazione chiavi software Microsoft incluso in Windows Server 2008 e Windows Vista e installato per impostazione predefinita.

L'isolamento delle chiavi è abilitato per impostazione predefinita in Windows Server 2008 e Windows Vista. La funzionalità di isolamento delle chiavi non è disponibile sulle piattaforme precedenti. Inoltre, i KSP di terze parti non vengono caricati nel servizio di isolamento chiave (processo LSA). Nel servizio di isolamento delle chiavi viene caricato solo il KSP Microsoft.

Il processo LSA viene usato come processo di isolamento della chiave per ottimizzare le prestazioni. Tutti gli accessi alle chiavi private passano attraverso il router di archiviazione chiavi, che espone un set completo di funzioni per la gestione e l'uso delle chiavi private.

CNG archivia la parte pubblica della chiave archiviata separatamente dalla parte privata. Anche la parte pubblica di una coppia di chiavi viene mantenuta nel servizio di isolamento delle chiavi ed è accessibile tramite la chiamata RPC (Remote Procedure Call) locale (LRPC). Il router di archiviazione chiavi usa LRPC durante la chiamata al processo di isolamento delle chiavi. Tutti gli accessi alle chiavi private passano attraverso il router di chiave privata e vengono controllati da CNG.

Come descritto in precedenza, è possibile supportare un'ampia gamma di dispositivi di archiviazione hardware. In ogni caso, l'interfaccia per tutti questi dispositivi di archiviazione è identica. Include funzioni per eseguire varie operazioni di chiave privata, oltre a funzioni che riguardano l'archiviazione e la gestione delle chiavi.

CNG fornisce un set di API che consentono di creare, archiviare e recuperare chiavi crittografiche. Per un elenco di queste API, vedere [funzioni di archiviazione delle chiavi CNG](cng-key-storage-functions.md).

## <a name="key-types"></a>Tipi di chiave

CNG supporta i tipi di chiave seguenti:

-   Diffie-Hellman chiavi pubbliche e private.
-   Chiavi pubbliche e private con algoritmo di firma digitale (DSA, FIPS 186-2).
-   \#Chiavi pubbliche e private RSA (PKCS 1).
-   Diverse chiavi pubbliche e private legacy (CryptoAPI).
-   Chiavi pubbliche e private di crittografia a curva ellittica.

## <a name="supported-algorithms"></a>Algoritmi supportati

CNG supporta gli algoritmi chiave seguenti.

| Algoritmo | Lunghezza chiave/hash (BITS)             |
|-----------|------------------------------------|
| RSA       | da 512 a 16384, in incrementi di 64 bit |
| DH        | da 512 a 16384, in incrementi di 64 bit |
| DSA       | da 512 a 1024, in incrementi di 64 bit  |
| ECDSA     | P-256, P-384, P-521 (curve NIST)  |
| ECDH      | P-256, P-384, P-521 (curve NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Directory e file principali

I CSP Microsoft CryptoAPI legacy archiviano le chiavi private nelle directory seguenti.

| Tipo di chiave                | Directory                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Utente privato            | % APPDATA% \\ Microsoft \\ Crypto \\ RSA \\ *utente SID*\\<br/>% APPDATA% \\ Microsoft \\ Crypto \\ DSS \\ *utente SID*\\<br/>                                                   |
| Privato sistema locale    | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-18\\<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-18\\<br/>   |
| Servizio locale privato   | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-19\\<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-19\\<br/>   |
| Servizio di rete privato | % ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-20\\<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-20\\<br/>   |
| Privato condiviso          | % ALLUSERSPROFILE% \\ dati applicazione \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys<br/>% ALLUSERSPROFILE% \\ Application Data \\ Microsoft \\ Crypto \\ DSS, \\ MachineKeys<br/> |



 

CNG archivia le chiavi private nelle directory seguenti.

| Tipo di chiave                | Directory                                                          |
|-------------------------|--------------------------------------------------------------------|
| Utente privato            | % APPDATA% \\ Microsoft \\ Crypto \\ chiavi                                 |
| Privato sistema locale    | % ALLUSERSPROFILE% \\ dati applicazione \\ Microsoft \\ Crypto \\ SystemKeys |
| Servizio locale privato   | % WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Servizio di rete privato | % WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Privato condiviso          | % ALLUSERSPROFILE% \\ dati applicazione \\ Microsoft \\ Crypto \\ Keys       |



 

Di seguito sono riportate alcune delle differenze tra i contenitori di chiavi CryptoAPI e CNG.

-   CNG utilizza nomi file diversi per i file di chiave rispetto ai file di chiave creati dal Rsaenh.dll e Dssenh.dll CSP legacy. Anche i file di chiave legacy hanno estensione. Key, ma i file di chiave CNG non hanno l'estensione. Key.
-   CNG supporta completamente i nomi dei contenitori di chiavi Unicode. CNG usa un hash del nome del contenitore Unicode, mentre CryptoAPI usa un hash del nome del contenitore ANSI.
-   CNG è più flessibile per quanto riguarda le coppie di chiavi RSA. Ad esempio, CNG supporta gli esponenti pubblici con una lunghezza superiore a 32 bit e supporta le chiavi in cui p e q sono lunghezze diverse.
-   In CryptoAPI il file contenitore di chiavi viene archiviato in una directory il cui nome è l'equivalente testuale del SID dell'utente. Questo non è più il caso in CNG, che elimina la difficoltà di trasferire gli utenti da un dominio a un altro senza perdere tutte le chiavi private.
-   Il provider di archiviazione chiavi e i nomi delle chiavi CNG sono limitati ai caratteri Unicode del **\_ percorso massimo** . Il CSP CryptoAPI e i nomi delle chiavi sono limitati ai caratteri ANSI del **\_ percorso massimo** .
-   CNG offre la funzionalità delle proprietà chiave definite dall'utente. Gli utenti possono creare e associare proprietà personalizzate con chiavi e archiviarle con chiavi salvate in modo permanente.

Quando si rende permanente una chiave, CNG può creare due file. Il primo file contiene la chiave privata nel nuovo formato CNG e viene sempre creato. Il file non può essere utilizzato dai DSN CryptoAPI legacy. Il secondo file contiene la stessa chiave privata nel contenitore di chiavi CryptoAPI legacy. Il secondo file è conforme al formato e alla posizione utilizzati dalla Rsaenh.dll. La creazione del secondo file si verifica solo se viene specificato il flag **NCRYPT \_ Write \_ Key \_ to \_ legacy \_ Store \_ flag** quando viene chiamata la funzione [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) per finalizzare una chiave RSA. Questa funzionalità non è supportata per le chiavi DSA e DH.

Quando un'applicazione tenta di aprire una chiave permanente esistente, CNG tenta innanzitutto di aprire il file CNG nativo. Se il file non esiste, CNG tenta di individuare una chiave corrispondente nel contenitore di chiavi CryptoAPI legacy.

Quando si spostano o si copiano le chiavi CryptoAPI da una macchina di origine a un computer di destinazione con Utilità di migrazione stato utente Windows (USMT), CNG non riuscirà ad accedere alle chiavi nel computer di destinazione. Per accedere a tali chiavi migrate, è necessario usare CryptoAPI.

 

 




