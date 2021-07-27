---
title: Firma Authenticode per sviluppatori di giochi
description: Questo articolo illustra come iniziare ad autenticare il gioco e come integrare l'autenticazione in un processo di compilazione giornaliero.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256b1cec0693787e76cfa479940524fca28d508e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436456"
---
# <a name="authenticode-signing-for-game-developers"></a>Firma Authenticode per sviluppatori di giochi

L'autenticazione dei dati è sempre più importante per gli sviluppatori di giochi. Windows Vista e Windows 7 hanno una serie di funzionalità, ad esempio il controllo genitori, che richiedono che i giochi siano firmati correttamente per garantire che nessuno abbia manomesso i dati. Microsoft Authenticode consente agli utenti finali e al sistema operativo di verificare che il codice del programma proviene dal legittimo proprietario e che non sia stato alterato o danneggiato accidentalmente. Questo articolo illustra come iniziare ad autenticare il gioco e come integrare l'autenticazione in un processo di compilazione giornaliero.

-   [Background](#background)
-   [Per iniziare](#getting-started)
-   [Uso di un'autorità di certificazione attendibile](#using-a-trusted-certificate-authority)
-   [Esempio di uso di un certificato di test](#example-using-a-test-certificate)
-   [Integrazione dell'accesso al codice nel sistema di compilazione giornaliero](#integrating-code-signing-into-the-daily-build-system)
-   [Revoca](#revocation)
-   [Driver per la firma del codice](#code-signing-drivers)
-   [Summary](#summary)
-   [Altre informazioni](#more-information)

> [!Note]  
> A partire dal 1° gennaio 2016, Windows 7 e versioni successive non considera più attendibile alcun certificato di firma del codice SHA-1 con una data di scadenza del 1° gennaio 2016 o successiva. Per [altre informazioni, Windows'imposizione della firma](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) del codice Authenticode e del timestamp.

 

## <a name="background"></a>Sfondo

I certificati digitali vengono usati per stabilire l'identità dell'autore. I certificati digitali vengono rilasciati da terze parti attendibili note come autorità di certificazione (CA), ad esempio VeriSign o Thawte. La CA è responsabile della verifica che il proprietario non reclami un'identificazione falsa. Dopo l'applicazione a una CA per un certificato, gli sviluppatori commerciali possono aspettarsi una risposta all'applicazione in meno di due settimane.

Dopo che la CA ha deciso di soddisfare i criteri, genera un certificato di firma del codice conforme a X.509, il formato di certificato standard del settore creato dall'International Telecommunications Union, con estensioni versione 3. Questo certificato identifica l'utente e contiene la chiave pubblica. Viene archiviato dalla CA per riferimento e una copia viene data elettronicamente. Allo stesso tempo, si crea anche una chiave privata, che è necessario mantenere al sicuro e che non è necessario condividere con nessuno, anche la CA.

Dopo aver creato una chiave pubblica e privata, è possibile iniziare a distribuire il software firmato. Microsoft offre strumenti per eseguire questa operazione in Windows SDK. Gli strumenti utilizzano un hash unidiredibile, producono un digest a lunghezza fissa e generano una firma crittografata con una chiave privata. Combinano quindi la firma crittografata con il certificato e le credenziali in una struttura nota come blocco di firma e la incorporano nel formato di file del file eseguibile. È possibile firmare qualsiasi tipo di file binario eseguibile, incluse DLL, file eseguibili e file cab.

La firma può essere verificata in diversi modi. I programmi possono chiamare la funzione CertVerifyCertificateChainPolicy e SignTool (signtool.exe) può essere usato per verificare una firma dal prompt della riga di comando. Windows Explorer include anche una scheda Firme digitali in Proprietà file che visualizza ogni certificato di un file binario firmato. La scheda Firme digitali viene visualizzata solo in Proprietà file per i file firmati. Inoltre, un'applicazione può essere autocertificata usando [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

La firma Authenticode non è utile solo per l'autenticazione dei dati da parte degli utenti finali, ma è necessaria anche per l'applicazione di patch agli account utente limitati e ai controlli genitori in Windows Vista e Windows 7. Inoltre, le tecnologie future nei sistemi operativi Windows possono richiedere la firma del codice, pertanto è consigliabile che tutti gli sviluppatori professionisti e professionisti acquisiscono un certificato di firma del codice da una CA. Altre informazioni su come eseguire questa operazione sono disponibili più avanti in questo articolo in [Uso di un'autorità di certificazione attendibile](#using-a-trusted-certificate-authority).

Il codice del gioco, i patcher e i programmi di installazione possono sfruttare ulteriormente la firma Authenticode verificando che i file siano autentici nel codice. Può essere usato per la sicurezza di rete generale e anti-trucchi. Il codice di esempio per controllare se un file è firmato è disponibile qui: Esempio di programma [C:](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)Verifica della firma di un file PE e codice di esempio per controllare la proprietà di un certificato di firma in un file firmato è disponibile qui: How To Get Information from Authenticode Signed Executables ( Come ottenere informazioni da file eseguibili [firmati Authenticode).](https://support.microsoft.com/kb/323809)

## <a name="getting-started"></a>Introduzione

Per iniziare, Microsoft offre strumenti con Visual Studio 2005 e Visual Studio 2008 e in [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)per eseguire e verificare il processo di firma del codice. Dopo aver installato Visual Studio o Windows SDK, gli strumenti descritti in questo articolo tecnico si trovano in una sottodirectory dell'installazione, che può includere uno o più degli elementi seguenti:

-   %SystemDrive% \\ Programmi \\ Microsoft Visual Studio 8 \\ SDK \\ v2.0 \\ Bin
-   %SystemDrive% \\ Programmi \\ Microsoft Visual Studio 8 \\ VC \\ PlatformSDK \\ Bin
-   %SystemDrive% \\ Programmi \\ Microsoft Visual Studio 9.0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   %SystemDrive% \\ Programmi Microsoft SDK Windows bin \\ \\ \\ v6.0A \\\\

Gli strumenti seguenti sono i più utili per la firma del codice:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Strumento di creazione certificati (MakeCert.exe)
</dt> <dd>

Genera un certificato X.509 di test, come file cer, che contiene la chiave pubblica e una chiave privata, come file con estensione pvk. Questo certificato è solo a scopo di test interno e non può essere usato pubblicamente.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Crea un file Exchange (pfx) di informazioni personali da una coppia di file con estensione cer e pvk. Il file con estensione pfx contiene sia la chiave pubblica che la chiave privata.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Firma il file usando il file con estensione pfx. SignTool supporta la firma di file DLL, file eseguibili, Windows Installer (.msi) e file cab (.cab).

</dd> </dl>

> [!Note]  
> Durante la lettura di altra documentazione, è possibile trovare riferimenti a SignCode (SignCode.exe), ma questo strumento è deprecato e non è più supportato. Usare invece SignTool.

 

## <a name="using-a-trusted-certificate-authority"></a>Uso di un'autorità di certificazione attendibile

Per ottenere un certificato attendibile, è necessario applicare a un'autorità di certificazione (CA), ad esempio VeriSign o Thawte. Microsoft non consiglia alcuna CA rispetto a un'altra, ma se si vuole eseguire l'integrazione nel servizio Segnalazione errori Windows (WER), è consigliabile usare VeriSign per rilasciare il certificato, perché l'accesso al database WER richiede un account WinQual che richiede un ID VeriSign. Per un elenco completo delle autorità di certificazione attendibili di terze parti, vedere [Microsoft Root Certificate Program Members](/previous-versions/ms995347(v=msdn.10)). Per altre informazioni sulla registrazione con WER, vedere "[Introduzione Segnalazione errori Windows](https://msdn.microsoft.com/)" nella [zona ISV](https://msdn.microsoft.com/).

Dopo aver ricevuto il certificato dalla CA, è possibile firmare il programma usando SignTool e rilasciare il programma al pubblico. È tuttavia necessario prestare attenzione a proteggere la chiave privata, contenuta nei file con estensione pfx e pvk. Assicurarsi di mantenere questi file in un percorso sicuro.

## <a name="example-using-a-test-certificate"></a>Esempio di uso di un certificato di test

La procedura seguente illustra la creazione di un certificato di firma del codice a scopo di test, seguita dalla firma di un programma di esempio Direct3D (denominato BasicHLSL.exe) con questo certificato di test. Questa procedura crea file con estensione cer e pvk, rispettivamente le chiavi pubbliche e private, che non possono essere usati per la certificazione pubblica.

In questo esempio viene aggiunto anche un timestamp alla firma. Un timestamp impedisce che la firma diventi non valida alla scadenza del certificato. Il codice firmato ma privo di timestamp non verrà convalidato dopo la scadenza del certificato. Pertanto, tutto il codice rilasciato pubblicamente deve avere un timestamp.

**Per creare un certificato e firmare un programma**

1.  Creare un certificato di test e una chiave privata usando lo strumento di creazione del certificato (MakeCert.exe).

    L'esempio della riga di comando seguente specifica MyPrivateKey come nome file per il file di chiave privata (con estensione pvk), MyPublicKey come nome del file di certificato (con estensione cer) e MySoftwareCompany come nome del certificato. Rende anche il certificato autofirmato, in modo che non abbia un'autorità radice non attendibile.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Creare un file di Exchange (con estensione pfx) di informazioni personali dal file di chiave privata (con estensione pvk) e dal file di certificato (con estensione cer) usando pvk2pfx.exe.

    Il file con estensione pfx combina le chiavi pubbliche e private in un singolo file. L'esempio della riga di comando seguente usa i file con estensione pvk e cer del passaggio precedente per creare il file con estensione pfx denominato MyPFX con la password della \_ password:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Firmare il programma con il file Exchange (con estensione pfx) con SignTool.

    È possibile specificare diverse opzioni nella riga di comando. L'esempio della riga di comando seguente usa il file con estensione pfx del passaggio precedente, assegna la password come password, specifica BasicHLSL come file da firmare e recupera un timestamp da un \_ server specificato:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > L'URL del servizio timestamp viene fornito dalla CA ed è facoltativo per il test. È importante che la firma di produzione includa un'autorità timestamp valida oppure la firma non verrà convalidata alla scadenza del certificato.

     

4.  Verificare che il programma sia firmato tramite SignTool.

    L'esempio della riga di comando seguente specifica che SignTool deve tentare di verificare la firma BasicHLSL.exe usando tutti i metodi disponibili fornendo al tempo stesso un output dettagliato:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    In questo esempio SignTool deve indicare che il certificato è collegato, pur dichiarando che non è attendibile, perché non viene emesso da una CA.

5.  Considerare attendibile il certificato di test.

    Per i certificati di test è necessario considerare attendibile il certificato. Questo passaggio deve essere ignorato per i certificati forniti da un'autorità di certificazione, in quanto questi verranno considerati attendibili per impostazione predefinita.

    Solo nei computer in cui si vuole considerare attendibile il certificato di test, eseguire quanto segue:

    ```
    certmgr.msc
    ```

    

    Fare quindi clic con il pulsante destro del Autorità di certificazione radice disponibile nell'elenco locale e scegliere Tutte le attività \| importa. Passare quindi al file con estensione pfx creato e seguire i passaggi della procedura guidata, inserendo il certificato nel Autorità di certificazione radice disponibile nell'elenco locale.

    Al termine della procedura guidata, è possibile avviare il test con il certificato attendibile nel computer.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrazione dell'accesso al codice nel sistema di compilazione giornaliero

Per integrare l'accesso al codice in un progetto, è possibile creare uno script o un file batch per eseguire gli strumenti da riga di comando. Dopo aver compilato il progetto, eseguire SignTool con le impostazioni appropriate (come illustrato nel passaggio 3 dell'esempio).

È necessario essere particolarmente cauti nel processo di compilazione per assicurare che l'accesso ai file con estensione pfx e pvk sia limitato al maggior numero possibile di computer e utenti. Come procedura consigliata, gli sviluppatori devono firmare il codice solo usando il certificato di test finché non sono pronti per la spedizione. Anche in questo caso, la chiave privata (con estensione pvk) deve essere mantenuta in una posizione protetta, ad esempio una stanza sicura o bloccata, e idealmente in un dispositivo crittografico, ad esempio un smart card.

Un altro livello di protezione viene fornito usando Microsoft Authenticode per firmare il pacchetto Windows Installer (MSI). Ciò consente di proteggere il pacchetto MSI da manomissioni e danneggiamenti accidentali. Per altre informazioni su come firmare pacchetti con Authenticode, vedere la documentazione dello strumento di creazione dell'msi.

## <a name="revocation"></a>Revoca

Se la sicurezza della chiave privata viene compromessa o un evento correlato alla sicurezza rende non valido un certificato Code-Signing, lo sviluppatore deve revocare il certificato. In questo modo, l'integrità dello sviluppatore e l'efficacia della firma del codice verrebbe compromessa. Un'autorità di certificazione può anche rilasciare una revoca con un orario specifico. Il codice firmato con un timestamp precedente all'ora di revoca verrà comunque considerato valido, ma il codice con un timestamp successivo non sarà valido. La revoca del certificato influisce sul codice in tutte le applicazioni firmate con il certificato revocato.

## <a name="code-signing-drivers"></a>Code-Signing driver

I driver possono e devono essere firmati con Authenticode. I driver in modalità kernel hanno requisiti aggiuntivi: le edizioni a 64 bit di Windows Vista e Windows 7 impediranno l'installazione di tutti i driver in modalità kernel non firmati e tutte le versioni di Windows presenteranno una richiesta di avviso quando un utente tenta di installare un driver non firmato. Gli amministratori possono inoltre impostare Criteri di gruppo per impedire l'installazione di driver non firmati in Microsoft Windows Server 2003, Windows XP Professional x64 Edition e nelle edizioni a 32 bit di Windows Vista e Windows 7.

Molti tipi di driver possono essere firmati con una firma attendibile da Microsoft, come parte del programma di certificazione Windows di [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) o [Unclassified Signature Program](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (precedentemente denominato Driver Reliability Signature), che consente al sistema di considerare completamente attendibili questi driver e installarli anche senza credenziali amministrative.

Come minimo, i driver devono essere firmati con Authenticode, perché i driver non firmati o autofirmati (ovvero firmati con un certificato di test) non verranno installati in molte piattaforme basate su Windows. Per altre informazioni sulla firma di driver e codice e sulle funzionalità correlate, vedere [Requisiti](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) di firma dei driver per Windows in [Windows Hardware Developer Central.](https://www.microsoft.com/whdc/)

## <a name="summary"></a>Riepilogo

L'uso di Microsoft Authenticode è un processo semplice. Dopo aver ottenuto un'area a esecuzione vincolata e creato una chiave privata, è semplice usare gli strumenti forniti da Microsoft. È quindi possibile abilitare funzionalità importanti in Windows Vista e Windows 7, ad esempio il controllo genitori, e in modo che i clienti sappiano che il prodotto proviene direttamente dal legittimo proprietario.

## <a name="more-information"></a>Altre informazioni

Per altre informazioni sugli strumenti e sui processi correlati alla firma del codice, vedere i collegamenti seguenti:

-   [Strumenti di crittografia](/windows/desktop/SecCrypto/cryptography-tools)
-   [Informazioni di riferimento per gli strumenti dell'API Crypto](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Panoramica di Authenticode e Turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificati digitali](/windows/desktop/SecCrypto/digital-certificates)
-   [Distribuzione di Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Procedura: Creare certificati temporanei da usare durante lo sviluppo](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
