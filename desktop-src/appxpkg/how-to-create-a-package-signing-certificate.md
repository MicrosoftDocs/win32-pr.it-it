---
title: Come creare un certificato di firma per pacchetti app
description: Informazioni su come usare MakeCert.exe e Pvk2Pfx.exe per creare un certificato di firma del codice di test, in modo che sia possibile firmare i pacchetti dell'app Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046568"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>Come creare un certificato di firma per pacchetti app

> [!IMPORTANT]
> MakeCert.exe è deprecato. Per informazioni aggiornate sulla creazione di un certificato, vedere [creare un certificato per la firma del pacchetto](/windows/msix/package/create-certificate-package-signing).

 

Informazioni su come usare [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) per creare un certificato di firma del codice di test, in modo che sia possibile firmare i pacchetti dell'app Windows.

È necessario firmare digitalmente le app di Windows in pacchetto prima di distribuirle. Se non si usa Microsoft Visual Studio 2012 per creare e firmare i pacchetti dell'app, è necessario creare e gestire i propri certificati di firma del codice. È possibile creare certificati usando [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) da Windows Driver Kit (WDK). È quindi possibile usare i certificati per firmare i pacchetti dell'app, in modo che possano essere distribuiti localmente per il test.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Distribuzione e pacchetti dell'applicazione](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Strumenti per la firma dei driver](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Prerequisiti

-   Strumenti di [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) da WDK

## <a name="instructions"></a>Istruzioni

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Passaggio 1: determinare il nome del server di pubblicazione del pacchetto

Per rendere il certificato di firma creato utilizzabile con il pacchetto dell'app che si vuole firmare, il nome del soggetto del certificato di firma deve corrispondere all'attributo **Publisher** dell'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel AppxManifest.xml per tale app. Si supponga, ad esempio, che il AppxManifest.xml contenga:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Per il parametro *PublisherName* specificato con l'utilità [**Makecert**](/windows-hardware/drivers/devtest/makecert) nel passaggio successivo, usare "CN = Contoso software, O = Contoso Corporation, C = US".

> [!Note]  
> Questa stringa di parametro è specificata tra virgolette e fa distinzione tra maiuscole e minuscole e spazi vuoti.

 

La stringa dell'attributo **Publisher** definita per l'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel AppxManifest.xml deve essere identica alla stringa specificata con il parametro [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n per il nome del soggetto del certificato. Copiare e incollare la stringa dove possibile.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Passaggio 2: creare una chiave privata utilizzando MakeCert.exe

Usare l'utilità [**Makecert**](/windows-hardware/drivers/devtest/makecert) per creare un certificato di prova autofirmato e una chiave privata:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Questo comando richiede di specificare una password per il file con estensione PVK. Si consiglia di scegliere una [password complessa](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) e di proteggere la chiave privata in un luogo sicuro.

Per questi motivi, è consigliabile usare i parametri suggeriti nell'esempio precedente:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Crea un certificato radice autofirmato. Ciò semplifica la gestione del certificato di test.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Contrassegna il vincolo di base per il certificato come entità finale. In questo modo si impedisce che il certificato venga usato come autorità di certificazione (CA) che può emettere altri certificati.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Imposta i valori di utilizzo chiavi avanzato (EKU) per il certificato.

> [!Note]  
> Non inserire uno spazio tra i due valori delimitati da virgole.

 

-   1.3.6.1.5.5.7.3.3 indica che il certificato è valido per la firma del codice. Specificare sempre questo valore per limitare l'utilizzo previsto per il certificato.
-   1.3.6.1.4.1.311.10.3.13 indica che il certificato rispetta la firma del ciclo di vita. In genere, se una firma viene contrassegnata con un timestamp, purché il certificato sia valido nel momento in cui è stato indicato il timestamp, la firma rimane valida anche se il certificato scade. Questo EKU impone la scadenza della firma, indipendentemente dal fatto che la firma sia contrassegnata con il timestamp.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Imposta la data di scadenza del certificato. Specificare un valore per il parametro *expirationDate* nel formato mm/gg/aaaa. Si consiglia di scegliere una data di scadenza solo se necessario a scopo di test, in genere inferiore a un anno. Questa data di scadenza insieme all'EKU per la firma di durata può contribuire a limitare la finestra in cui il certificato può essere compromesso e usato in modo improprio.

</dd> </dl>

Per altre informazioni sulle altre opzioni, vedere [**Makecert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Passaggio 3: creare un file di scambio di informazioni personali (con estensione pfx) usando Pvk2Pfx.exe

Usare l'utilità [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) per convertire i file con estensione PVK e CER creati da [**Makecert**](/windows-hardware/drivers/devtest/makecert) in un file con estensione pfx che è possibile usare con [SignTool](/windows/desktop/SecCrypto/signtool) per firmare un pacchetto dell'app:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

I file *myKey. PVK* e *myKey. cer* sono gli stessi che [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) creati nel passaggio precedente. Utilizzando il parametro facoltativo/po, è possibile specificare una password diversa per il file con estensione pfx risultante; in caso contrario, il file con estensione pfx ha la stessa password di *myKey. PVK*.

Per ulteriori informazioni sulle altre opzioni, vedere [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Commenti

Dopo aver creato il file con estensione pfx, è possibile usare il file con [SignTool](/windows/desktop/SecCrypto/signtool) per firmare un pacchetto dell'app. Per altre informazioni, vedere [come firmare un pacchetto dell'app usando SignTool](how-to-sign-a-package-using-signtool.md). Ma il certificato non è ancora considerato attendibile dal computer locale per la distribuzione dei pacchetti dell'app finché non viene installato nell'archivio certificati attendibili del computer locale. È possibile utilizzare [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), disponibile in Windows.

**Per installare i certificati con WindowsCertutil.exe**

1.  Eseguire **Cmd.exe** come amministratore.
2.  Eseguire questo comando:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Si consiglia di rimuovere i certificati se non sono più in uso. Dallo stesso prompt dei comandi dell'amministratore eseguire questo comando:

``` syntax
Certutil -delStore TrustedPeople certID
```

**CertID** è il numero di serie del certificato. Eseguire questo comando per determinare il numero di serie del certificato:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Aggiungendo un certificato agli [archivi certificati del computer locale](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), si influisce sull'attendibilità del certificato di tutti gli utenti del computer. Si consiglia di installare i certificati di firma del codice desiderati per testare i pacchetti dell'applicazione nell'archivio certificati persone attendibili. Rimuovere tempestivamente questi certificati quando non sono più necessari, per impedire che vengano usati per compromettere l'attendibilità del sistema.

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

[Come firmare un pacchetto di app con SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Firma di un pacchetto di app](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 