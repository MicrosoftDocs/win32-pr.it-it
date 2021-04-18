---
title: Firma Authenticode per sviluppatori di giochi
description: Questo articolo illustra come iniziare a eseguire l'autenticazione del gioco e come integrare l'autenticazione in un processo di compilazione giornaliero.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f304e6cc8e185264699709987f62dfdca17bf8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300088"
---
# <a name="authenticode-signing-for-game-developers"></a>Firma Authenticode per sviluppatori di giochi

L'autenticazione dei dati è sempre più importante per gli sviluppatori di giochi. Windows Vista e Windows 7 hanno diverse funzionalità, ad esempio i controlli padre, che richiedono che i giochi siano firmati correttamente per assicurarsi che nessuno abbia alterato i dati. Microsoft Authenticode consente agli utenti finali e al sistema operativo di verificare che il codice del programma provenga dal legittimo proprietario e che non sia stato alterato in modo dannoso o accidentalmente danneggiato. Questo articolo illustra come iniziare a eseguire l'autenticazione del gioco e come integrare l'autenticazione in un processo di compilazione giornaliero.

-   [Background](#background)
-   [Per iniziare](#getting-started)
-   [Uso di un'autorità di certificazione attendibile](#using-a-trusted-certificate-authority)
-   [Esempio di utilizzo di un certificato di prova](#example-using-a-test-certificate)
-   [Integrazione del codice per l'accesso al sistema di compilazione giornaliero](#integrating-code-signing-into-the-daily-build-system)
-   [Revoca](#revocation)
-   [Driver per la firma del codice](#code-signing-drivers)
-   [Summary](#summary)
-   [Altre informazioni](#more-information)

> [!Note]  
> A partire dal 1 ° gennaio 2016, Windows 7 e versioni successive non considerano più attendibile il certificato di firma del codice SHA-1 con una data di scadenza pari al 1 ° gennaio 2016 o successiva. Per altre informazioni, vedere [applicazione di Windows per la firma e il timestamp del codice Authenticode](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) .

 

## <a name="background"></a>Sfondo

I certificati digitali vengono usati per stabilire l'identità dell'autore. I certificati digitali vengono emessi da terze parti attendibili, nota come autorità di certificazione (CA), ad esempio VeriSign o Thawte. La CA è responsabile della verifica che il proprietario non stia reclamando un'identificazione falsa. Dopo aver applicato una CA per un certificato, gli sviluppatori commerciali possono prevedere una risposta alla propria applicazione in meno di due settimane.

Dopo che l'autorità di certificazione ha deciso di soddisfare i criteri dei criteri, genera un certificato di firma codice conforme a X. 509, il formato di certificato standard del settore creato dall'Unione internazionale delle telecomunicazioni, con le estensioni della versione 3. Questo certificato identifica l'utente e contiene la chiave pubblica. Viene archiviato dalla CA come riferimento e viene fornita una copia elettronica. Allo stesso tempo, si crea anche una chiave privata che è necessario proteggere e che non si deve condividere con nessuno, neanche con la CA.

Quando si dispone di una chiave pubblica e privata, è possibile iniziare a distribuire il software firmato. Microsoft fornisce gli strumenti per eseguire questa operazione nel Windows SDK. Gli strumenti utilizzano un hash unidirezionale, producono un digest a lunghezza fissa e generano una firma crittografata con una chiave privata. Combinano quindi la firma crittografata con il certificato e le credenziali in una struttura nota come blocco di firma e la incorporano nel formato del file eseguibile. È possibile firmare qualsiasi tipo di file binario eseguibile, incluse le dll, i file eseguibili e i file CAB.

La firma può essere verificata in diversi modi. I programmi possono chiamare la funzione CertVerifyCertificateChainPolicy e SignTool (signtool.exe) può essere usato per verificare una firma dal prompt della riga di comando. Esplora risorse dispone inoltre di una scheda firme digitali in proprietà file che consente di visualizzare ogni certificato di un file binario firmato. La scheda firme digitali viene visualizzata solo nelle proprietà dei file firmati. Inoltre, un'applicazione può eseguire la verifica automatica usando [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

La firma Authenticode non è utile solo per l'autenticazione dei dati da parte degli utenti finali, ma è necessaria anche per l'applicazione di patch a account utente limitati e a controlli padre in Windows Vista e Windows 7. Inoltre, le tecnologie future nei sistemi operativi Windows possono richiedere anche che il codice sia firmato, quindi è consigliabile che tutti gli sviluppatori professionisti e amatoriali acquisiscano un certificato di firma codice da un'autorità di certificazione. Altre informazioni su come eseguire questa operazione sono disponibili più avanti in questo articolo in [uso di un'autorità di certificazione attendibile](#using-a-trusted-certificate-authority).

Il codice del gioco, i Patcher e i programmi di installazione possono sfruttare ulteriormente la firma Authenticode verificando che i file siano autentici nel codice. Questa operazione può essere usata per l'anti-cheat e la sicurezza di rete generale. Il codice di esempio per verificare se un file è firmato è disponibile qui: [esempio C programma: verifica della firma di un file PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)e codice di esempio per verificare la proprietà di un certificato di firma in un file firmato sono disponibili qui: [come ottenere informazioni da file eseguibili firmati da Authenticode](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Introduzione

Per iniziare, Microsoft fornisce strumenti con Visual Studio 2005 e Visual Studio 2008, oltre che nel [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx), per facilitare l'esecuzione e la verifica del processo di firma del codice. Dopo l'installazione di Visual Studio o del Windows SDK, gli strumenti descritti in questo articolo tecnico si trovano in una sottodirectory dell'installazione, che può includere uno o più dei seguenti elementi:

-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ SDK \\ v 2.0 \\ bin
-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ VC \\ platformsdk \\ bin
-   % SystemDrive% \\ Program Files \\ Microsoft Visual Studio 9,0 \\ smartdevices \\ SDK \\ SDKTools\\
-   % SystemDrive% \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 un \\ contenitore\\

Gli strumenti seguenti sono i più utili per la firma del codice:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Strumento per la creazione di certificati (MakeCert.exe)
</dt> <dd>

Genera un certificato X. 509 di test, come file con estensione cer, che contiene la chiave pubblica e una chiave privata, come file con estensione PVK. Questo certificato è solo a scopo di test interno e non può essere utilizzato pubblicamente.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Crea un file di scambio di informazioni personali (con estensione pfx) da una coppia di file con estensione CER e PVK. Il file con estensione pfx contiene sia la chiave pubblica che quella privata.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Firma il file usando il file con estensione pfx. SignTool supporta la firma di file DLL, file eseguibili, file di Windows Installer (MSI) e file CAB (CAB).

</dd> </dl>

> [!Note]  
> Durante la lettura di altra documentazione, è possibile trovare riferimenti a SignCode (SignCode.exe), ma questo strumento è deprecato e non è più supportato. in alternativa, usare SignTool.

 

## <a name="using-a-trusted-certificate-authority"></a>Uso di un'autorità di certificazione attendibile

Per ottenere un certificato attendibile, è necessario applicare a un'autorità di certificazione (CA), ad esempio VeriSign o Thawte. Microsoft non consiglia alcuna CA rispetto a un'altra, ma se si vuole eseguire l'integrazione nel servizio Segnalazione errori Windows (WER), è consigliabile usare VeriSign per emettere il certificato, perché l'accesso al database WER richiede un account WinQual che richiede un ID VeriSign. Per un elenco completo di autorità di certificazione di terze parti attendibili, vedere [membri del programma Microsoft Root Certificate](/previous-versions/ms995347(v=msdn.10)). Per ulteriori informazioni sulla registrazione con WER, vedere l'argomento "[introduzione segnalazione errori Windows](https://msdn.microsoft.com/)" nella [zona ISV](https://msdn.microsoft.com/).

Dopo aver ricevuto il certificato dalla CA, è possibile firmare il programma usando SignTool e rilasciare il programma al pubblico. Tuttavia, è necessario prestare attenzione a proteggere la chiave privata, che è contenuta nei file. pfx e. PVK. Assicurarsi di tenere questi file in una posizione sicura.

## <a name="example-using-a-test-certificate"></a>Esempio di utilizzo di un certificato di prova

I passaggi seguenti illustrano la creazione di un certificato di firma codice a scopo di test, seguito dalla firma di un programma di esempio Direct3D (denominato BasicHLSL.exe) con questo certificato di test. Questa procedura consente di creare i file con estensione CER e PVK, rispettivamente le chiavi pubbliche e private, che non possono essere usate per la certificazione pubblica.

In questo esempio viene aggiunto anche un timestamp alla firma. Un timestamp impedisce che la firma diventi non valida al momento della scadenza del certificato. Il codice firmato ma privo di timestamp non verrà convalidato dopo la scadenza del certificato. Pertanto, tutti i codici rilasciati pubblicamente dovrebbero avere un timestamp.

**Per creare un certificato e firmare un programma**

1.  Creare un certificato di prova e una chiave privata utilizzando lo strumento di creazione dei certificati (MakeCert.exe).

    Il seguente esempio di riga di comando specifica MyPrivateKey come nome file per il file di chiave privata (con estensione PVK), MyPublicKey come nome file per il file del certificato (con estensione CER) e MySoftwareCompany come nome del certificato. Il certificato viene inoltre reso autofirmato, in modo che non disponga di un'autorità radice non attendibile.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Creare un file di scambio di informazioni personali (con estensione pfx) dal file di chiave privata (con estensione PVK) e dal file del certificato (con estensione CER) usando pvk2pfx.exe.

    Il file con estensione pfx combina le chiavi pubbliche e private in un unico file. Il seguente esempio di riga di comando usa i file con estensione PVK e CER del passaggio precedente per creare il file con estensione pfx denominato MyPFX con la password \_ :

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Firmare il programma con il file di scambio di informazioni personali (con estensione pfx) usando SignTool.

    È possibile specificare diverse opzioni nella riga di comando. Il seguente esempio di riga di comando usa il file con estensione pfx del passaggio precedente, assegna la \_ password come password, specifica BasicHLSL come file da firmare e recupera un timestamp da un server specificato:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > L'URL del servizio timestamp viene fornito dalla CA ed è facoltativo per il test. È importante che la firma di produzione includa un'autorità di certificazione del timestamp valida o che la firma non venga convalidata al termine del certificato.

     

4.  Verificare che il programma sia firmato tramite SignTool.

    Il seguente esempio di riga di comando specifica che SignTool deve tentare di verificare la firma su BasicHLSL.exe usando tutti i metodi disponibili fornendo output dettagliato:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    In questo esempio, SignTool deve indicare che il certificato è collegato, indicando anche che non è attendibile, perché non viene emesso da un'autorità di certificazione.

5.  Considerare attendibile il certificato di prova.

    Per i certificati di test è necessario considerare attendibile il certificato. Questo passaggio deve essere ignorato per i certificati forniti da una CA, perché saranno considerati attendibili per impostazione predefinita.

    Solo nei computer in cui si desidera considerare attendibile il certificato di test, eseguire il comando seguente:

    ```
    certmgr.msc
    ```

    

    Fare clic con il pulsante destro del mouse su autorità di certificazione radice attendibili e scegliere tutte le attività \| Importa. Individuare quindi il file con estensione pfx creato e seguire i passaggi della procedura guidata, inserendo il certificato nelle autorità di certificazione radice attendibili.

    Al termine della procedura guidata, è possibile avviare il test con il certificato attendibile nel computer.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrazione del codice per l'accesso al sistema di compilazione giornaliero

Per integrare la firma del codice in un progetto, è possibile creare un file batch o uno script per eseguire gli strumenti da riga di comando. Dopo aver compilato il progetto, eseguire SignTool con le impostazioni appropriate (come illustrato nel passaggio 3 dell'esempio).

Prestare particolare attenzione al processo di compilazione per garantire che l'accesso ai file con estensione pfx e PVK sia limitato al minor numero di computer e utenti possibile. Come procedura consigliata, gli sviluppatori devono firmare il codice solo usando il certificato di test fino a quando non sono pronti per la spedizione. Anche in questo caso, la chiave privata (con estensione PVK) deve essere mantenuta in una posizione protetta, ad esempio una stanza sicura o bloccata, e idealmente su un dispositivo crittografico, ad esempio una smart card.

Un altro livello di protezione viene fornito tramite Microsoft Authenticode per firmare il pacchetto di Windows Installer (MSI). Ciò consente di proteggere il pacchetto MSI da manomissioni e danneggiamenti accidentali. Per altre informazioni su come firmare i pacchetti con Authenticode, fare riferimento alla documentazione per lo strumento di creazione MSI.

## <a name="revocation"></a>Revoca

Nel caso in cui la sicurezza della chiave privata venga compromessa o un evento correlato alla sicurezza esegua il rendering di un certificato di Code-Signing non valido, lo sviluppatore deve revocare il certificato. Questa operazione potrebbe indebolire l'integrità dello sviluppatore e l'efficacia del codice di firma. Una CA può inoltre emettere una revoca con un'ora specifica; il codice firmato con un timestamp prima dell'ora di revoca verrà comunque considerato valido, ma il codice con un timestamp successivo non sarà valido. La revoca dei certificati influiscono sul codice in tutte le applicazioni firmate con il certificato revocato.

## <a name="code-signing-drivers"></a>Driver Code-Signing

I driver possono e devono avere firma Authenticode. I driver in modalità kernel presentano requisiti aggiuntivi: le edizioni a 64 bit di Windows Vista e Windows 7 impediranno l'installazione di tutti i driver in modalità kernel senza firma e tutte le versioni di Windows presenteranno una richiesta di avviso quando un utente tenta di installare un driver non firmato. Inoltre, gli amministratori possono impostare Criteri di gruppo per impedire l'installazione di driver non firmati in Microsoft Windows Server 2003, Windows XP Professional x64 Edition e versioni a 32 bit di Windows Vista e Windows 7.

Molti tipi di driver possono essere firmati con una firma attendibile di Microsoft, come parte del programma di certificazione Windows di [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) o del [programma di firma non classificato](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (denominato in precedenza driver affidabilità), che consente al sistema di considerare completamente attendibili questi driver e di installarli anche senza credenziali amministrative.

Come minimo, i driver devono essere firmati con Authenticode, perché i driver non firmati o autofirmati, ovvero firmati con un certificato di prova, non possono essere installati in molte piattaforme basate su Windows. Per ulteriori informazioni sulla firma di driver e codice e sulla funzionalità correlata, vedere [driver signing requirements for Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Riepilogo

L'utilizzo di Microsoft Authenticode è un processo semplice. Una volta ottenuta una CER e creato una chiave privata, è semplice utilizzare gli strumenti forniti da Microsoft. È quindi possibile abilitare funzionalità importanti in Windows Vista e Windows 7, ad esempio i controlli padre, e informare i clienti che il prodotto deriva direttamente dal legittimo proprietario.

## <a name="more-information"></a>Ulteriori informazioni

Per ulteriori informazioni sugli strumenti e i processi correlati alla firma del codice, vedere i collegamenti seguenti:

-   [Strumenti di crittografia](/windows/desktop/SecCrypto/cryptography-tools)
-   [Informazioni di riferimento sugli strumenti dell'API Crypto](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Panoramica di Authenticode e turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificati digitali](/windows/desktop/SecCrypto/digital-certificates)
-   [Distribuzione di Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Procedura: creare certificati temporanei da usare durante lo sviluppo](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 