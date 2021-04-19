---
title: Come firmare il pacchetto di un'app tramite SignTool
description: Informazioni su come usare SignTool per firmare i pacchetti dell'app Windows in modo che possano essere distribuiti.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300602"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Come firmare il pacchetto di un'app tramite SignTool

> [!Note]  
> Per la firma di un pacchetto dell'app Windows, vedere [firmare un pacchetto dell'app con SignTool](/windows/msix/package/sign-app-package-using-signtool).

 

Informazioni su come usare [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti dell'app Windows in modo che possano essere distribuiti. [**SignTool**](/windows-hardware/drivers/devtest/signtool) fa parte del Software Development Kit (SDK) di Windows.

Per poter distribuire tutti i pacchetti dell'app Windows, è necessario firmarli digitalmente. Mentre Microsoft Visual Studio 2012 e versioni successive possono firmare un pacchetto dell'app durante la sua creazione, i pacchetti creati con lo strumento [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) del Windows SDK non sono firmati.

> [!Note]  
> È possibile utilizzare [**SignTool**](/windows-hardware/drivers/devtest/signtool) solo per firmare i pacchetti dell'app Windows in Windows 8 e versioni successive o windows Server 2012 e versioni successive. Non è possibile usare **SignTool** per firmare i pacchetti dell'app nei sistemi operativi di livello inferiore, ad esempio Windows 7 o windows Server 2008 R2.

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Distribuzione e pacchetti dell'applicazione](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Strumenti per firmare i file e controllare le firme](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Prerequisiti

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), che fa parte dell'Windows SDK
-   Un certificato di firma codice valido, ad esempio, un file di scambio di informazioni personali (con estensione pfx) creato con gli strumenti [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)

    Per informazioni sulla creazione di un certificato di firma codice valido, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).

-   App di Windows in pacchetto, ad esempio un file con estensione appx creato con lo strumento [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)

**Altre considerazioni**

Il certificato usato per firmare il pacchetto dell'app deve soddisfare i criteri seguenti:

-   Il nome del soggetto del certificato deve corrispondere all'attributo del **server di pubblicazione** contenuto nell'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del file AppxManifest.xml archiviato nel pacchetto. Il nome del server di pubblicazione fa parte dell'identità di un'app di Windows in pacchetto, quindi è necessario fare in modo che il nome del soggetto del certificato corrisponda al nome dell'editore dell'app. Ciò consente di verificare l'identità dei pacchetti firmati rispetto alla firma digitale. Per informazioni sugli errori di firma che possono derivare dalla firma di un pacchetto dell'app con [**SignTool**](/windows-hardware/drivers/devtest/signtool), vedere la sezione Osservazioni di [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).
-   Il certificato deve essere valido per la firma del codice. Ciò significa che entrambi gli elementi devono essere true:

    -   Il campo utilizzo chiavi avanzato (EKU) del certificato deve essere annullato o contenere il valore EKU per la firma del codice (1.3.6.1.5.5.7.3.3).
    -   Il campo utilizzo chiavi (KU) del certificato deve essere annullato o contenere il bit Usage per la firma digitale (0x80).

-   Il certificato contiene una chiave privata.
-   Il certificato è valido. È attivo, non è scaduto e non è stato revocato.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Passaggio 1: determinare l'algoritmo hash da usare

Quando si firma il pacchetto dell'app, è necessario usare lo stesso algoritmo hash usato al momento della creazione del pacchetto dell'app. Se sono state usate le impostazioni predefinite per creare il pacchetto dell'app, l'algoritmo hash usato è SHA256.

Se è stato usato il pacchetto di app con un algoritmo hash specifico per creare il pacchetto dell'app, usare lo stesso algoritmo per la firma del pacchetto. Per determinare l'algoritmo hash da utilizzare per la firma di un pacchetto, è possibile estrarre il contenuto del pacchetto ed esaminare il file di AppxBlockMap.xml. L'attributo **HashMethod** dell'elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica l'algoritmo hash usato durante la creazione del pacchetto dell'applicazione. Ad esempio:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

L'elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) precedente indica che è stato usato l'algoritmo SHA256. Questa tabella elenca il mapping degli algoritmi attualmente disponibili:

| Valore **HashMethod**                            | *HashAlgorithm* da usare |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (appx predefinito) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Passaggio 2: eseguire SignTool.exe per firmare il pacchetto

**Per firmare il pacchetto con un certificato di firma da un file con estensione pfx**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) imposta come valore predefinito il parametro/FD *HashAlgorithm* su SHA1 se non è specificato e SHA1 non è valido per la firma dei pacchetti dell'app. Quindi, è necessario specificare questo parametro quando si firma un pacchetto dell'app. Per firmare un pacchetto dell'app creato con l'hash SHA256 predefinito, è necessario specificare il parametro *HashAlgorithm* di/FD come SHA256:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

È possibile omettere il parametro/p *password* se si usa un file con estensione pfx che non è protetto da password. È anche possibile usare altre opzioni di selezione dei certificati supportate da [**SignTool**](/windows-hardware/drivers/devtest/signtool) per firmare i pacchetti dell'applicazione. Per altre informazioni su queste opzioni, vedere [SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> Non è possibile usare l'operazione timestamp di [**SignTool**](/windows-hardware/drivers/devtest/signtool) in un pacchetto dell'app firmato; l'operazione non è supportata.

 

Se si vuole indicare il timestamp del pacchetto dell'app, è necessario eseguire questa operazione durante l'operazione di firma. Ad esempio:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Rendere il parametro/TR *timestampServerUrl* uguale all'URL per un server di timestamp RFC 3161.

## <a name="remarks"></a>Commenti

Questa sezione illustra la risoluzione dei problemi relativi agli errori di firma per i pacchetti dell'applicazione.

### <a name="troubleshooting-app-package-signing-errors"></a>Risoluzione degli errori di firma del pacchetto dell'app

Oltre agli errori di firma che [**SignTool**](/windows-hardware/drivers/devtest/signtool) può restituire, **SignTool** può restituire anche errori specifici per la firma dei pacchetti dell'applicazione. Questi errori vengono in genere visualizzati come errori interni:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Se il codice di errore inizia con 0x8008, ad esempio 0x80080206 \_ appx \_ E \_ contenuto danneggiato, significa che il pacchetto firmato non è valido. In questo caso, prima di poter firmare il pacchetto, è necessario ricompilare il pacchetto. Per l'elenco completo degli \* errori 0x8008, vedere [**codici di errore com (sicurezza e configurazione)**](/windows/desktop/com/com-error-codes-4).

Più comunemente, l'errore è 0x8007000B (errore \_ nel \_ formato errato). In questo caso, è possibile trovare informazioni più specifiche sull'errore nel registro eventi:

**Per eseguire una ricerca nel registro eventi**

1.  Eseguire eventvwr. msc.
2.  Aprire il registro eventi: Visualizzatore eventi (locale) > registri applicazioni e servizi > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational
3.  Cercare l'evento di errore più recente.

L'errore interno generalmente corrisponde a uno dei seguenti:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>ID evento</th>
<th>Esempio di stringa di evento</th>
<th>Suggerimento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>150</td>
<td>errore 0x8007000B: il nome del server di pubblicazione del manifesto dell'applicazione (CN = Contoso) deve corrispondere al nome del soggetto del certificato di firma (CN = Contoso, C = US).</td>
<td>Il nome del server di pubblicazione del manifesto dell'applicazione deve corrispondere esattamente al nome del soggetto della firma.
<blockquote>
[!Note]<br />
Questi nomi sono specificati tra virgolette e sono sensibili a maiuscole e minuscole.
</blockquote>
<br/> È possibile aggiornare la stringa dell'attributo del <strong>server di pubblicazione</strong> definita per l'elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> nel file di AppxManifest.xml in modo che corrisponda al nome del soggetto del certificato di firma designato. In alternativa, selezionare un certificato di firma diverso con un nome soggetto corrispondente al nome del server di pubblicazione del manifesto dell'applicazione. Il nome del server di pubblicazione del manifesto e il nome del soggetto del certificato sono entrambi elencati nel messaggio di evento.</td>
</tr>
<tr class="even">
<td>151</td>
<td>errore 0x8007000B: il metodo hash della firma specificato (SHA512) deve corrispondere al metodo hash usato nella mappa del blocco del pacchetto dell'app (SHA256).</td>
<td>L'oggetto hashAlgorithm specificato nel parametro/FD non è corretto (vedere passaggio 1: determinare l'algoritmo hash da usare). Eseguire di nuovo <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> con l'oggetto HashAlgorithm che corrisponde alla mappa del blocco del pacchetto dell'app.</td>
</tr>
<tr class="odd">
<td>152</td>
<td>errore 0x8007000B: il contenuto del pacchetto dell'app deve essere convalidato rispetto alla mappa dei blocchi.</td>
<td>Il pacchetto dell'app è danneggiato e deve essere ricompilato per generare una nuova mappa a blocchi. Per altre informazioni sulla creazione di un pacchetto dell'app, vedere Creazione di un pacchetto dell'app con <a href="make-appx-package--makeappx-exe-.md">app Packager</a> o <a href="/previous-versions/hh975357(v=vs.110)">creazione di un pacchetto dell'app con Visual Studio 2012</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Dopo la firma del pacchetto, il certificato utilizzato per firmare il pacchetto deve essere ancora considerato attendibile dal computer in cui deve essere distribuito il pacchetto. Aggiungendo un certificato agli [archivi certificati del computer locale](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), si influisce sull'attendibilità del certificato di tutti gli utenti del computer. Si consiglia di installare i certificati di firma del codice desiderati per testare i pacchetti dell'applicazione nell'archivio certificati persone attendibili e rimuovere tempestivamente tali certificati quando non sono più necessari. Se si creano certificati di test personalizzati per la firma dei pacchetti dell'app, è anche consigliabile limitare i privilegi associati al certificato di test. Per altre informazioni sulla creazione di certificati di test per la firma dei pacchetti dell'app, vedere [come creare un certificato di firma del pacchetto dell'app](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Esempi**
</dt> <dt>

[Esempio di creare un pacchetto dell'app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
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

