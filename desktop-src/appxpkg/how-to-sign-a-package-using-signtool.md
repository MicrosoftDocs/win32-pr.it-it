---
title: Come firmare il pacchetto di un'app tramite SignTool
description: Informazioni su come usare SignTool per firmare i pacchetti Windows'app in modo che possano essere distribuiti.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4e4c0941cbcced30053b8fd31e44100adc9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474887"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Come firmare il pacchetto di un'app tramite SignTool

> [!Note]  
> Per la firma di Windows pacchetto dell'app, vedere [Firmare un pacchetto dell'app usando SignTool.](/windows/msix/package/sign-app-package-using-signtool)

 

Informazioni su come usare [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti Windows'app in modo che possano essere distribuiti. [**SignTool**](/windows-hardware/drivers/devtest/signtool) fa parte di Windows Software Development Kit (SDK).

Tutti Windows pacchetti dell'app devono essere firmati digitalmente prima di poter essere distribuiti. Anche se Microsoft Visual Studio 2012 e versioni successive possono firmare un pacchetto dell'app durante la creazione, i pacchetti creati usando lo strumento di creazione pacchetti [dell'app (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) di Windows SDK non vengono firmati.

> [!Note]  
> È possibile usare [**SignTool solo per**](/windows-hardware/drivers/devtest/signtool) firmare i pacchetti Windows'app in Windows 8 e versioni successive o Windows Server 2012 e versioni successive. Non è possibile usare **SignTool** per firmare i pacchetti dell'app in sistemi operativi di livello inferiore, ad esempio Windows 7 o Windows Server 2008 R2.

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Pacchetti di app e distribuzione](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Strumenti per firmare file e controllare le firme](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Prerequisiti

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), che fa parte di Windows SDK
-   Un certificato di firma del codice valido, ad esempio un file PFX (Personal Information Exchange) creato con gli strumentiMakeCert.exe [**ePvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) sicurezza [](/windows-hardware/drivers/devtest/makecert)

    Per informazioni sulla creazione di un certificato di firma del codice valido, vedere Come creare un certificato di [firma del pacchetto dell'app.](how-to-create-a-package-signing-certificate.md)

-   Un'app Windows pacchetto, ad esempio un file con estensione appx creato usando lo strumento di creazione pacchetti [dell'app (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)

**Considerazioni aggiuntive**

Il certificato utilizzato per firmare il pacchetto dell'app deve soddisfare questi criteri:

-   Il nome del soggetto del certificato deve corrispondere **all'attributo Publisher** contenuto nell'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del file AppxManifest.xml archiviato all'interno del pacchetto. Il nome dell'editore fa parte dell'identità di un'app Windows in pacchetto, pertanto è necessario fare in modo che il nome soggetto del certificato corrisponda al nome dell'editore dell'app. Ciò consente di verificare l'identità dei pacchetti firmati rispetto alla firma digitale. Per informazioni sugli errori di firma che possono verificarsi durante la firma di un pacchetto dell'app con [**SignTool,**](/windows-hardware/drivers/devtest/signtool)vedere la sezione Osservazioni di Come creare un certificato di firma del [pacchetto dell'app.](how-to-create-a-package-signing-certificate.md)
-   Il certificato deve essere valido per la firma del codice. Ciò significa che entrambi questi elementi devono essere true:

    -   Il campo Extended Key Usage (EKU) del certificato deve essere non impostato o contenere il valore EKU per la firma del codice (1.3.6.1.5.5.7.3.3).
    -   Il campo Utilizzo chiavi (KU) del certificato deve essere non impostato o contenere il bit di utilizzo per la firma digitale (0x80).

-   Il certificato contiene una chiave privata.
-   Il certificato è valido. È attivo, non è scaduto e non è stato revocato.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Passaggio 1: Determinare l'algoritmo hash da usare

Quando si firma il pacchetto dell'app, è necessario usare lo stesso algoritmo hash usato durante la creazione del pacchetto dell'app. Se sono stati usati impostazioni predefinite per creare il pacchetto dell'app, l'algoritmo hash usato è SHA256.

Se è stato usato lo strumento di creazione pacchetti dell'app con un algoritmo hash specifico per creare il pacchetto dell'app, usare lo stesso algoritmo per firmare il pacchetto. Per determinare l'algoritmo hash da utilizzare per la firma di un pacchetto, è possibile estrarre il contenuto del pacchetto ed esaminare il file AppxBlockMap.xml file. **L'attributo HashMethod** dell'elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica l'algoritmo hash usato durante la creazione del pacchetto dell'app. Ad esempio:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

L'elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) precedente indica che è stato usato l'algoritmo SHA256. Questa tabella elenca il mapping degli algoritmi attualmente disponibili:

| **Valore HashMethod**                            | *hashAlgorithm* da usare |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (impostazione predefinita.appx) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Passaggio 2: Eseguire SignTool.exe per firmare il pacchetto

**Per firmare il pacchetto con un certificato di firma da un file con estensione pfx**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) consente di impostare il parametro *hashAlgorithm* /fd come predefinito su SHA1 se non è specificato e SHA1 non è valido per la firma dei pacchetti dell'app. Pertanto, è necessario specificare questo parametro quando si firma un pacchetto dell'app. Per firmare un pacchetto dell'app creato con l'hash SHA256 predefinito, specificare il parametro /fd *hashAlgorithm* come SHA256:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

È possibile omettere il parametro /p *password* se si usa un file con estensione pfx che non è protetto da password. È anche possibile usare altre opzioni di selezione del certificato supportate da [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti dell'app. Per altre informazioni su queste opzioni, vedere [SignTool.](/windows/desktop/SecCrypto/signtool)

> [!Note]  
> Non è possibile usare [**l'operazione timestamp SignTool**](/windows-hardware/drivers/devtest/signtool) su un pacchetto di app firmato. L'operazione non è supportata.

 

Se si vuole impostare il timestamp per il pacchetto dell'app, è necessario farlo durante l'operazione di firma. Ad esempio:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Rendere il parametro /tr *timestampServerUrl* uguale all'URL per un server timestamp RFC 3161.

## <a name="remarks"></a>Commenti

Questa sezione illustra la risoluzione degli errori di firma per i pacchetti dell'app.

### <a name="troubleshooting-app-package-signing-errors"></a>Risoluzione degli errori di firma dei pacchetti dell'app

Oltre agli errori di firma che [**SignTool**](/windows-hardware/drivers/devtest/signtool) può restituire, **SignTool** può anche restituire errori specifici della firma dei pacchetti dell'app. Questi errori vengono in genere visualizzati come errori interni:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Se il codice di errore inizia con 0x8008, ad esempio 0x80080206 APPX E CORRUPT CONTENT, indica che il pacchetto firmato \_ \_ non è \_ valido. In questo caso, prima di poter firmare il pacchetto, è necessario ricompilare il pacchetto. Per l'elenco completo degli \* 0x8008, vedere [**Codici di errore COM (sicurezza e installazione).**](/windows/desktop/com/com-error-codes-4)

Più comunemente, l'errore è 0x8007000b (ERROR \_ BAD \_ FORMAT). In questo caso, è possibile trovare informazioni più specifiche sugli errori nel registro eventi:

**Per eseguire ricerche nel registro eventi**

1.  Eseguire Eventvwr.msc.
2.  Aprire il registro eventi: Visualizzatore eventi (local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational
3.  Cercare l'evento di errore più recente.

L'errore interno corrisponde in genere a uno dei seguenti:


| ID evento | Stringa di evento di esempio | Suggerimento | 
|----------|----------------------|------------|
| 150 | errore 0x8007000B: il nome dell'autore del manifesto dell'app (CN=Contoso) deve corrispondere al nome soggetto del certificato di firma (CN=Contoso, C=US). | Il nome dell'autore del manifesto dell'app deve corrispondere esattamente al nome del soggetto della firma.<blockquote>[!Note]<br />Questi nomi sono specificati tra virgolette e distinzione tra maiuscole e minuscole e spazi vuoti.</blockquote><br /> È possibile aggiornare <strong>la Publisher</strong> dell'attributo definito per l'elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> nel file AppxManifest.xml in modo che corrisponda al nome soggetto del certificato di firma previsto. In caso contrario, selezionare un certificato di firma diverso con un nome soggetto corrispondente al nome dell'autore del manifesto dell'app. Il nome dell'autore del manifesto e il nome del soggetto del certificato sono entrambi elencati nel messaggio dell'evento. | 
| 151 | errore 0x8007000B: il metodo hash della firma specificato (SHA512) deve corrispondere al metodo hash usato nella mappa a blocchi del pacchetto dell'app (SHA256). | L'hashAlgorithm specificato nel parametro /fd non è corretto (vedere Passaggio 1: Determinare l'algoritmo hash da usare). Eseguire nuovamente <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool con</strong></a> l'hashAlgorithm che corrisponde alla mappa di blocchi del pacchetto dell'app. | 
| 152 | errore 0x8007000B: il contenuto del pacchetto dell'app deve essere convalidato rispetto alla mappa a blocchi. | Il pacchetto dell'app è danneggiato e deve essere ricompilato per generare una nuova mappa a blocchi. Per altre informazioni sulla creazione di un pacchetto dell'app, vedi Creazione di un pacchetto dell'app con il <a href="make-appx-package--makeappx-exe-.md">packager dell'app</a> o Creazione di un pacchetto <a href="/previous-versions/hh975357(v=vs.110)">dell'app con Visual Studio 2012.</a> | 




 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Dopo la firma del pacchetto, il certificato utilizzato per firmare il pacchetto deve comunque essere considerato attendibile dal computer in cui il pacchetto deve essere distribuito. L'aggiunta di un certificato [agli archivi certificati del](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)computer locale influisce sull'attendibilità del certificato di tutti gli utenti nel computer. È consigliabile installare i certificati di firma del codice desiderati per testare i pacchetti dell'app nell'archivio certificati Persone attendibili e rimuovere tempestivamente tali certificati quando non sono più necessari. Se si creano certificati di test personalizzati per la firma dei pacchetti dell'app, è anche consigliabile limitare i privilegi associati al certificato di test. Per altre informazioni sulla creazione di certificati di test per la firma dei pacchetti dell'app, vedere [Come creare un certificato di firma del pacchetto dell'app.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Esempi**
</dt> <dt>

[Esempio di creazione di un pacchetto dell'app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Concetti**
</dt> <dt>

[Procedure consigliate per la firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Firma di un pacchetto in Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[App Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[Come creare un certificato di firma del pacchetto di un'app](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

